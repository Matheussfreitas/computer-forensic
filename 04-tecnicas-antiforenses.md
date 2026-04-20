# Tecnicas Antiforenses

## Conceito

Tecnicas antiforenses sao praticas utilizadas para dificultar, atrasar, confundir ou impedir a identificacao de evidencias durante uma investigacao digital. Conforme indicado nas anotacoes, essas tecnicas podem ocorrer por meio de ocultacao, codificacao ou exclusao de vestigios.

O objetivo central da antiforense e interferir nos resultados da investigacao.

## Principais tecnicas mencionadas

### Criptografia

A criptografia protege o conteudo dos dados, tornando-os inacessiveis sem a chave correta. Em contexto legitimo, ela e um mecanismo de seguranca. Em contexto investigativo, pode dificultar o acesso a arquivos, discos, mensagens e backups.

### Impacto pericial

- impede leitura direta do conteudo;
- exige obtencao de senhas, chaves ou artefatos de desbloqueio;
- aumenta a importancia da analise viva, pois chaves podem estar carregadas na memoria.

### Esteganografia

A esteganografia consiste em esconder informacao dentro de outro arquivo, como imagens, audios ou videos. Diferente da criptografia, que embaralha o conteudo, a esteganografia procura esconder a propria existencia da mensagem.

### Exemplo

Um arquivo de imagem aparentemente comum pode conter texto, documentos ou comandos ocultos sem alteracao visual perceptivel ao usuario.

### Sanitizacao de discos

As anotacoes definem esse processo como formatacao bit a bit. Em termos gerais, a sanitizacao corresponde a tecnicas destinadas a sobrescrever ou destruir os dados de forma a dificultar ou inviabilizar a recuperacao posterior.

### Objetivo

- eliminar vestigios recuperaveis;
- impedir restauracao por ferramentas forenses;
- destruir dados sensiveis de forma definitiva.

### Evolucao tecnologica

A evolucao tecnologica tambem pode atuar como barreira antiforense, ainda que de forma indireta. Novos sistemas, dispositivos, formatos e mecanismos de seguranca tornam a investigacao mais complexa.

### Exemplos

- armazenamento em nuvem;
- criptografia nativa de dispositivos;
- autenticacao multifator;
- sistemas distribuidos;
- aplicativos com mensagens efemeras.

Isso exige atualizacao constante das tecnicas e ferramentas periciais.

### Rootkits

Rootkits sao conjuntos de tecnicas ou programas criados para esconder processos, arquivos, conexoes ou a propria presenca de malware no sistema.

### Risco para a investigacao

- ocultacao de artefatos;
- adulteracao da visao do sistema operacional;
- interferencia na coleta de evidencias;
- manutencao de acesso clandestino.

### Desmagnetizador

O uso de desmagnetizador pode inutilizar dados gravados em determinadas midias magneticas ao alterar seu estado fisico. Trata-se de um metodo extremo de destruicao de evidencias.

### Consequencia

Quando aplicado corretamente sobre midias compativeis, pode inviabilizar a recuperacao do conteudo.

### Empacotamento

Empacotamento, ou packing, e o processo de comprimir, cifrar ou encapsular executaveis para dificultar analise estatica e identificacao do codigo real.

### Uso comum

- ocultacao de malware;
- evasao de antivirus;
- dificultar engenharia reversa.

### Anti-debugging

Sao tecnicas inseridas em softwares para detectar ou impedir o uso de depuradores. O programa pode encerrar a execucao, alterar o comportamento ou fornecer resultados enganosos quando identifica que esta sendo analisado.

### Anti-disassembly

Consiste em empregar artificios para confundir ferramentas de desmontagem de codigo, dificultando a leitura do fluxo real de instrucoes.

### Anti-VM

Tecnicas anti-VM tentam detectar se o programa esta sendo executado em maquina virtual. Quando isso acontece, o software pode:

- deixar de executar a carga maliciosa;
- encerrar a aplicacao;
- simular comportamento inocente.

Isso e comum em amostras maliciosas criadas para escapar de analise em ambientes controlados.

## Relevancia para a computacao forense

Conhecer tecnicas antiforenses e tao importante quanto dominar tecnicas forenses. O perito precisa ser capaz de reconhecer sinais de ocultacao, destruicao ou manipulacao de dados para:

- explicar limitacoes da investigacao;
- adotar estrategias adequadas de coleta;
- justificar a necessidade de analise viva;
- escolher ferramentas especializadas;
- interpretar corretamente a ausencia de vestigios.

## Conclusao

As tecnicas antiforenses representam um desafio real para o trabalho pericial. Criptografia, esteganografia, sanitizacao, rootkits e mecanismos de evasao mostram que a ausencia ou a dificuldade de acesso a evidencias nem sempre significa inexistencia de atividade. Muitas vezes, significa que houve tentativa deliberada de ocultacao.
