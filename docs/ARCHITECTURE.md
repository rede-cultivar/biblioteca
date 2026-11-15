# Arquitetura de Referência

**Versão:** 0.1 — Documento inicial  
**Status:** Em discussão comunitária

## 1. Objetivo

Este documento estabelece princípios e diretrizes para a arquitetura tecnológica da iniciativa.

Não representa uma especificação definitiva nem determina antecipadamente todas as tecnologias que serão utilizadas.

Seu objetivo é orientar a avaliação de alternativas e evitar decisões que comprometam a interoperabilidade, a autonomia das bibliotecas ou a sustentabilidade do ecossistema.

## 2. Princípios arquiteturais

A arquitetura deverá observar os seguintes princípios:

### 2.1. Descentralização

A rede não deverá depender de uma única instalação centralizada para funcionar.

Bibliotecas poderão manter seus próprios sistemas e infraestrutura, conforme seus recursos e necessidades.

### 2.2. Interoperabilidade

A comunicação entre componentes deverá utilizar interfaces documentadas e protocolos abertos sempre que possível.

### 2.3. Modularidade

Os componentes deverão possuir responsabilidades bem definidas.

A substituição de um sistema de gestão bibliotecária, por exemplo, não deverá exigir a reconstrução de toda a infraestrutura de comunicação federada.

### 2.4. Autonomia operacional

Cada biblioteca deverá manter controle sobre suas operações locais e suas políticas administrativas.

### 2.5. Privacidade desde a concepção

A arquitetura deverá limitar a circulação de dados pessoais e impedir a publicação automática de informações privadas.

### 2.6. Sustentabilidade

A solução deverá considerar os custos de hospedagem, manutenção, atualização, suporte e capacitação.

### 2.7. Software livre

A arquitetura deverá favorecer componentes livres, documentados e passíveis de auditoria.

## 3. Visão lógica

A arquitetura poderá ser organizada em camadas conceituais.

### 3.1. Camada de gestão bibliotecária

Responsável pelas operações internas de cada biblioteca:

- Catalogação.
- Cadastro de exemplares.
- Circulação.
- Empréstimos.
- Reservas.
- Gestão de leitores.
- Relatórios administrativos.

Essa camada poderá ser implementada por sistemas existentes, como o Koha, ou por outras soluções avaliadas pela comunidade.

### 3.2. Camada de integração

Responsável por conectar os sistemas bibliotecários às demais partes do ecossistema.

Possíveis responsabilidades:

- Adaptar modelos de dados.
- Consultar interfaces externas.
- Sincronizar informações selecionadas.
- Controlar permissões de publicação.
- Processar eventos.
- Gerenciar identificadores externos.
- Registrar erros e inconsistências.

A existência de um componente intermediário próprio dependerá da avaliação das integrações disponíveis.

### 3.3. Camada federada

Responsável pela comunicação com o Fediverso.

Poderá utilizar ActivityPub para:

- Publicação de atividades.
- Perfis públicos de bibliotecas.
- Divulgação de eventos.
- Comunicação com outras instâncias.
- Compartilhamento de informações públicas.

A compatibilidade com plataformas específicas deverá ser testada, especialmente quando houver extensões ou modelos próprios.

### 3.4. Camada social de leitura

Responsável pelas experiências sociais relacionadas à leitura.

A integração com BookWyrm deverá ser priorizada como alternativa a desenvolver uma rede social própria.

A iniciativa poderá oferecer mecanismos de conexão e descoberta, mas não deverá replicar desnecessariamente as funcionalidades sociais já existentes.

### 3.5. Camada de apresentação

Responsável pelas interfaces utilizadas por bibliotecas, leitores e organizações.

Poderá incluir:

- Interface administrativa.
- Consulta pública de catálogos.
- Páginas de bibliotecas.
- Diretório de participantes.
- Interfaces de descoberta.
- Integrações com plataformas externas.

As interfaces deverão ser acessíveis e adequadas a diferentes dispositivos.

## 4. Modelo de implantação

A arquitetura deverá permitir diferentes configurações de implantação.

### 4.1. Instalação independente

Uma biblioteca poderá utilizar um sistema de gestão bibliotecária próprio e participar da rede por meio de integrações compatíveis.

### 4.2. Infraestrutura compartilhada

Bibliotecas com poucos recursos poderão utilizar serviços compartilhados, desde que existam garantias de isolamento, privacidade, autonomia administrativa e portabilidade dos dados.

### 4.3. Instalação comunitária

Grupos de bibliotecas poderão organizar infraestruturas coletivas para compartilhar custos e responsabilidades operacionais.

Nenhum modelo deverá ser imposto como obrigatório.

## 5. Integrações e contratos

As integrações deverão ser documentadas por meio de contratos claros.

Sempre que possível, deverão especificar:

- Formatos de entrada e saída.
- Identificadores utilizados.
- Regras de autenticação.
- Permissões necessárias.
- Tratamento de erros.
- Política de repetição de operações.
- Comportamento diante de indisponibilidade.
- Regras de atualização e exclusão.
- Compatibilidade entre versões.

Interfaces públicas deverão evitar dependência de detalhes internos de implementação.

## 6. Modelo de dados

A arquitetura deverá distinguir entidades que possuem significados diferentes.

Entre elas:

- Obra.
- Edição.
- Exemplar.
- Biblioteca.
- Leitor.
- Empréstimo.
- Reserva.
- Evento.
- Resenha.
- Avaliação.
- Lista de leitura.

Uma obra pode possuir várias edições. Uma edição pode possuir vários exemplares em diferentes bibliotecas.

O ISBN deverá ser tratado como identificador de uma edição ou publicação específica, e não como identificador universal de uma obra.

Os dados administrativos de circulação deverão permanecer separados das informações públicas de descoberta e comunicação.

## 7. Eventos e sincronização

A comunicação entre sistemas poderá utilizar mecanismos orientados a eventos, quando isso trouxer benefícios reais.

Exemplos de eventos internos:

- Nova obra catalogada.
- Novo exemplar cadastrado.
- Exemplar disponibilizado.
- Evento cultural publicado.
- Nova aquisição divulgada.

Nem todo evento interno deverá ser publicado externamente.

A publicação deverá passar por regras explícitas de autorização, filtragem e transformação dos dados.

O sistema deverá considerar:

- Duplicidade de mensagens.
- Entrega atrasada.
- Indisponibilidade temporária.
- Reprocessamento.
- Consistência entre sistemas.
- Atualizações e exclusões.

## 8. Segurança

A arquitetura deverá considerar:

- Autenticação segura.
- Autorização baseada em responsabilidades.
- Isolamento entre bibliotecas.
- Proteção de credenciais.
- Criptografia em trânsito.
- Gestão segura de segredos.
- Registro de operações administrativas relevantes.
- Atualizações de segurança.
- Estratégias de backup e recuperação.
- Proteção contra abuso de interfaces públicas.

Os mecanismos específicos serão definidos durante o desenho técnico.

## 9. Observabilidade e operação

Os componentes deverão oferecer meios de acompanhar sua operação.

Sempre que possível, deverão existir:

- Logs estruturados.
- Métricas operacionais.
- Monitoramento de disponibilidade.
- Rastreamento de falhas de integração.
- Alertas administrativos.
- Procedimentos de backup.
- Procedimentos de restauração.

Os registros operacionais não deverão armazenar dados pessoais desnecessários.

## 10. Portabilidade e continuidade

As bibliotecas deverão ter condições de exportar seus dados em formatos documentados.

A arquitetura deverá evitar aprisionamento tecnológico e dependência irreversível de fornecedores.

A documentação deverá contemplar:

- Instalação.
- Configuração.
- Atualização.
- Backup.
- Restauração.
- Migração.
- Exportação de dados.
- Desinstalação e substituição de componentes.

## 11. Critérios para escolha tecnológica

A seleção de tecnologias deverá considerar:

1. Licença de software.
2. Maturidade do projeto.
3. Comunidade e manutenção.
4. Documentação.
5. Segurança.
6. Interoperabilidade.
7. Facilidade de implantação.
8. Requisitos de infraestrutura.
9. Custos operacionais.
10. Capacidade de manutenção por colaboradores da comunidade.
11. Portabilidade dos dados.
12. Adequação às necessidades das bibliotecas.

A familiaridade da equipe com uma tecnologia poderá ser considerada, mas não deverá ser o único critério.

## 12. Decisões arquiteturais

Decisões relevantes deverão ser registradas em `docs/decisions/`.

Cada registro deverá conter:

- Contexto.
- Problema ou necessidade.
- Alternativas consideradas.
- Decisão adotada.
- Justificativa.
- Consequências.
- Data e participantes da decisão.

Decisões que afetem autonomia, privacidade, governança ou interoperabilidade deverão ser submetidas à discussão comunitária.

## 13. Questões em aberto

Ainda deverão ser avaliados:

- Sistema de gestão bibliotecária de referência.
- Necessidade de middleware próprio.
- Modelo de implantação compartilhada.
- Estratégia de integração com BookWyrm.
- Estratégia de descoberta de catálogos.
- Modelo de autenticação entre componentes.
- Formatos bibliográficos prioritários.
- Estratégia de sincronização.
- Tecnologias de backend e frontend.
- Infraestrutura de hospedagem e operação.

Este documento deverá evoluir à medida que essas decisões forem tomadas.