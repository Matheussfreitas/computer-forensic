# Tecnicas Forenses

## Introducao

As tecnicas forenses sao os metodos usados para localizar, recuperar, interpretar e correlacionar evidencias digitais. A tecnica escolhida depende do tipo de crime, do dispositivo analisado e do objetivo da investigacao.

## A tecnica depende do caso

Nem toda investigacao exige o mesmo tipo de evidencia. Alguns exemplos:

- acesso nao autorizado: evidencias de conexao e autenticacao;
- pornografia: fotos, videos e artefatos de armazenamento;
- abuso de comunicacao: emails, cabecalhos, logs e anexos;
- incidentes de rede: trafego, portas, conexoes e dispositivos intermediarios.

## Areas relacionadas de atuacao

Tambem e importante ampliar a visao sobre o campo forense, considerando frentes como:

- computacao forense tradicional;
- forense em dispositivos moveis;
- forense digital em redes;
- forense em Internet das Coisas;
- forense em banco de dados.

Cada uma dessas areas muda tanto o tipo de artefato coletado quanto as ferramentas mais adequadas.

## Analise de vulnerabilidade e teste de penetracao

Embora nao sejam a mesma coisa que analise forense, essas praticas se relacionam com seguranca e ajudam a compreender incidentes:

- **analise de vulnerabilidade**: identifica fragilidades e mede exposicao a riscos;
- **teste de penetracao**: tenta explorar vulnerabilidades para verificar o impacto real.

Metodologias comuns de pentest incluem OWASP, ISSAF, NIST, OSSTMM e PTES. Em contexto forense, esse conhecimento ajuda a entender como um sistema pode ter sido comprometido.

## Exploracao dos MAC times

Os MAC times correspondem aos tempos associados aos arquivos, especialmente:

- modificacao;
- acesso;
- criacao ou alteracao de metadados, conforme o sistema de arquivos.

Esses tempos permitem montar a linha temporal dos fatos, responder quando um arquivo foi criado ou alterado e verificar se determinado evento ocorreu antes ou depois de outro.

### Aplicacoes

- construcao de timelines;
- correlacao com logs e eventos;
- deteccao de manipulacao de arquivos;
- identificacao de atividade de usuarios.

### Cuidados

Copias, restauracoes, sincronizacao, backup ou o proprio sistema operacional podem alterar metadados. Por isso, os MAC times nunca devem ser interpretados isoladamente.

## Ordem de volatilidade

A ordem de volatilidade define o que deve ser coletado primeiro quando o sistema ainda esta ativo. A logica geral e:

1. memoria e estado de execucao;
2. conexoes de rede e processos ativos;
3. arquivos temporarios;
4. disco local;
5. midias persistentes e backups.

Essa prioridade evita a perda de evidencias que desaparecem assim que a maquina e desligada ou sofre alteracoes.

## Data carving

O data carving e uma tecnica de recuperacao baseada em assinaturas conhecidas de arquivos, sem depender necessariamente da estrutura do sistema de arquivos.

### Quando e util

- arquivos apagados;
- particoes corrompidas;
- sistema de arquivos danificado;
- tentativa de ocultacao de vestigios.

### Como funciona

A ferramenta procura cabecalhos, rodapes ou marcadores binarios tipicos de formatos como JPEG, PDF, ZIP e outros, tentando reconstruir o arquivo a partir dos blocos encontrados.

### Limitacoes

- pode recuperar arquivos incompletos;
- pode perder nomes e caminhos originais;
- pode gerar falsos positivos;
- sofre impacto da fragmentacao da midia.

## Analise de email

O cabecalho de email e uma das fontes mais importantes de metadados em investigacoes de fraude, phishing, ameaca, assedio e falsidade ideologica.

### O que observar

- remetente aparente e remetente real;
- servidores pelos quais a mensagem passou;
- horarios de envio e recebimento;
- enderecos IP;
- identificadores de mensagem;
- resultados de autenticacao.

Esses elementos ajudam a validar a origem da mensagem e identificar inconsistencias.

## Outras observacoes

Tambem e importante considerar o estudo de evidencias em comunicacoes, como email e aplicativos de mensagem, alem da importancia de recursos audiovisuais e de interpretacao contextual em determinados casos.

## Conclusao

As tecnicas forenses transformam dados brutos em evidencias compreensiveis. O uso combinado de MACTimes, ordem de volatilidade, data carving e analise de email aumenta a capacidade de reconstruir fatos e sustentar conclusoes tecnicas com mais seguranca.
