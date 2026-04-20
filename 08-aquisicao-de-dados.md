# Aquisicao de Dados

## Objetivo

Este arquivo resume a aquisicao de dados em computacao forense, cobrindo formatos de imagem, metodos de aquisicao, validacao, RAID e coleta remota.

## Tipos de aquisicao

Existem dois modelos principais.

### Aquisicao estatica

E a copia de um disco ou dispositivo a partir de um sistema desligado. Foi durante muito tempo o padrao preferido porque tende a nao alterar os dados e pode ser repetida com mais previsibilidade.

### Aquisicao ao vivo

E a coleta feita com o sistema em execucao. Ganhou importancia por causa de:

- criptografia de disco;
- necessidade de capturar RAM;
- interesse em processos e conexoes ativos.

Apesar de muito util, esse tipo de aquisicao altera o estado do sistema e nao pode ser reproduzido exatamente da mesma forma.

## Termos equivalentes

Varios termos sao usados quase como sinonimos:

- copia de fluxo de bits;
- imagem de fluxo de bits;
- imagem;
- espelho;
- copia de setor.

## Formatos de armazenamento

### Formato raw

E o formato classico gerado por ferramentas como `dd`. Trata-se de copia bit a bit do dispositivo.

#### Vantagens

- transferencia rapida;
- ampla compatibilidade com ferramentas forenses;
- simplicidade.

#### Desvantagens

- ocupa espaco equivalente ao volume original;
- pode ter dificuldade com setores problematicos;
- exige armazenamento separado dos hashes e metadados.

### Formatos proprietarios

Oferecem recursos adicionais, como:

- compactacao opcional;
- segmentacao em varios arquivos;
- verificacao de integridade por segmento;
- armazenamento de metadados do caso.

O formato Expert Witness, com extensoes como `.E01`, tornou-se um padrao nao oficial amplamente suportado.

### AFF

O Formato Forense Avancado foi apresentado como alternativa aberta, extensivel e multiplataforma, com suporte a:

- imagens compactadas ou nao;
- metadados integrados;
- verificacoes internas de consistencia;
- segmentacao sem a mesma limitacao tradicional de tamanho.

## Metodos de aquisicao

Quatro metodos principais sao:

### Disco para arquivo de imagem

E o metodo mais comum. Cria um arquivo de imagem bit a bit que pode ser copiado, armazenado e analisado posteriormente.

### Disco para disco

Usado quando a copia para arquivo nao e viavel, por exemplo em casos de incompatibilidade de hardware ou software, especialmente com discos antigos.

### Aquisicao logica

Captura apenas arquivos ou pastas especificos de interesse para a investigacao, como emails ou documentos determinados.

### Aquisicao esparsa

Semelhante a logica, mas inclui tambem alguns elementos adicionais, como arquivos excluidos relevantes para o caso.

## Compactacao e backup

A compactacao sem perdas pode reduzir bastante o tamanho de uma imagem, embora arquivos que ja estejam compactados nao tragam grande ganho adicional.

Backup em fita tambem pode ser usado como alternativa para grandes volumes, apesar de sua lentidao.

## Planejamento de contingencia

Algumas precaucoes importantes para aquisicao segura sao:

- criar copia duplicada da imagem;
- produzir pelo menos duas imagens;
- usar ferramentas ou tecnicas diferentes, quando possivel;
- copiar tambem areas protegidas do host;
- estar preparado para lidar com discos criptografados.

## Discos criptografados

A criptografia mudou bastante o processo de aquisicao. Se a maquina estiver ligada, uma aquisicao ao vivo pode capturar o conteudo descriptografado. Se nao estiver, o acesso pode depender de:

- chave;
- senha;
- artefatos de desbloqueio;
- tecnicas especializadas.

## Protecao contra escrita

O objetivo e impedir qualquer alteracao no dispositivo original. Sistemas operacionais podem escrever no disco automaticamente apenas ao inicializar ou montar a unidade, o que exige mecanismos de protecao contra gravacao.

Por isso, o uso de live CDs forenses e configuracoes de somente leitura e especialmente importante.

## Linux Live CD e ferramentas classicas

Distribuicoes Linux preparadas para forense sao usadas com foco em nao montar midias em modo de escrita.

### `dd`

Ferramenta tradicional de copia de dados.

#### Pontos positivos

- cria imagem raw legivel por varias ferramentas;
- e amplamente conhecida.

#### Limitacoes

- nao foi criada especificamente para uso forense;
- nao compacta dados;
- exige maior cuidado operacional.

### `dcfldd`

Extensao do `dd` com recursos mais adequados a forense, como:

- multiplas opcoes de hash;
- registro de erros;
- exibicao de progresso;
- segmentacao;
- verificacao da imagem contra a midia original.

## Validacao de aquisicoes

A validacao e um dos pontos mais criticos da computacao forense. Ela normalmente usa algoritmos de hash, como:

- CRC-32;
- MD5;
- SHA-1;
- variantes mais fortes, como SHA-256 e superiores.

### Em Linux

Em Linux, e comum usar `md5sum`, `sha1sum` e opcoes de hash do `dcfldd`.

### Em Windows

No Windows, a validacao costuma depender de utilitarios de terceiros ou dos proprios recursos internos das ferramentas comerciais.

## RAID

Sistemas RAID trazem desafios adicionais por causa do volume de dados, do nivel de RAID utilizado e da forma como a ferramenta interpreta a estrutura distribuida ou espelhada.

Em resumo:

- RAID 0: foco em desempenho e capacidade, sem redundancia;
- RAID 1: espelhamento e recuperacao;
- RAID 5: distribuicao com paridade.

Na aquisicao de RAID, e preciso avaliar:

- quanto armazenamento sera necessario;
- qual tipo de RAID esta em uso;
- se a ferramenta suporta a estrutura copiada;
- se a analise exigira imagem conjunta ou volumes separados.

## Aquisicao remota

Tambem existem ferramentas de aquisicao por rede, capazes de copiar dados de maquinas em uso.

### Vantagens

- permite coleta em sistemas remotos;
- viabiliza captura ao vivo;
- pode incluir RAM e informacoes volateis.

### Desvantagens

- dependencia da rede;
- risco de atrasos ou erros por trafego intenso;
- necessidade de permissoes adequadas;
- possibilidade de bloqueio por antivirus ou controles internos.

Entre os exemplos citados estao ProDiscover e EnCase Enterprise.

## Conclusao

A aquisicao de dados e uma etapa central da computacao forense. Escolher o metodo correto, preservar a integridade do original, validar a copia e entender limitacoes de criptografia, RAID e coleta remota sao fatores decisivos para a confiabilidade da investigacao.
