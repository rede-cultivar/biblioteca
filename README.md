<p align="center">
  <img src="assets/branding/logo-provisorio.png" alt="Logotipo provisório da Rede de Bibliotecas" width="200">
</p>

<h1 align="center">Rede de Bibliotecas</h1>

<p align="center">
  <strong>Uma iniciativa comunitária em construção para conectar bibliotecas, leitores e comunidades por meio de uma infraestrutura livre, descentralizada e federada.</strong>
</p>

<p align="center">
  <a href="#documentação"><img alt="Documentação em português" src="https://img.shields.io/badge/documenta%C3%A7%C3%A3o-portugu%C3%AAs-blue"></a>
  <a href="LICENSE"><img alt="Licença: AGPL-3.0" src="https://img.shields.io/badge/licen%C3%A7a-AGPL--3.0-blueviolet"></a>
  <img alt="Fediverso" src="https://img.shields.io/badge/fediverso-ActivityPub-6f42c1">
  <img alt="Status: em construção" src="https://img.shields.io/badge/status-em%20constru%C3%A7%C3%A3o-yellow">
  <a href="governance/CONTRIBUTING.md"><img alt="Contribuições bem-vindas" src="https://img.shields.io/badge/contribui%C3%A7%C3%B5es-bem--vindas-brightgreen"></a>
</p>

> **Nome e identidade visual provisórios.** A definição definitiva será feita
> coletivamente pela comunidade, conforme a
> [Carta de Fundação](governance/CHARTER.md) e a
> [Política de Marca e Identidade](governance/TRADEMARK_POLICY.md).

## Sobre o projeto

A Rede de Bibliotecas é uma iniciativa comunitária que está construindo uma
infraestrutura digital livre para bibliotecas independentes, comunitárias,
populares, públicas, escolares, universitárias e outras organizações dedicadas à
democratização do acesso à leitura e ao conhecimento.

A proposta é conectar acervos, leitores e comunidades por meio de uma rede
aberta e federada: administrar acervos bibliográficos, facilitar a circulação de
livros, compartilhar informações bibliográficas e fortalecer comunidades de
leitura — sem exigir que as bibliotecas abandonem seus sistemas, suas políticas
ou suas formas próprias de organização.

A iniciativa busca integrar sistemas de gerenciamento de bibliotecas ao
Fediverso, utilizando o protocolo ActivityPub e promovendo a interoperabilidade
com plataformas como o BookWyrm.

O projeto não pertence a uma pessoa ou organização específica. Sua identidade,
governança e evolução são construídas coletivamente e documentadas publicamente
neste repositório.

## O que estamos construindo

- **Gestão bibliotecária:** catalogação de obras e edições, cadastro de
  exemplares, controle de disponibilidade, empréstimos, devoluções, reservas e
  relatórios administrativos.
- **Descoberta e compartilhamento:** consulta aos catálogos de bibliotecas
  participantes, divulgação de novas aquisições, listas temáticas e coleções.
- **Experiência social de leitura:** integração com o BookWyrm para descoberta
  de resenhas, avaliações, recomendações e clubes de leitura.
- **Comunicação federada:** perfis públicos de bibliotecas, divulgação de
  eventos e comunicados por meio do ActivityPub e do Fediverso.
- **Cooperação entre bibliotecas:** compartilhamento de informações
  bibliográficas, intercâmbio de experiências e ações conjuntas.
- **Privacidade:** controle do leitor sobre o que é publicado, com históricos de
  empréstimo privados por padrão.

A iniciativa não pretende ser uma plataforma comercial de venda de livros, uma
rede social centralizada, um substituto do BookWyrm ou um sistema único
obrigatório para todas as bibliotecas. Também não pretende tornar públicos dados
pessoais ou históricos de empréstimos dos leitores.

## Princípios

- Justiça social e democratização do conhecimento.
- Solidariedade e cooperação comunitária.
- Cultura, informação e conhecimento como bens comuns.
- Autonomia e descentralização.
- Participação e construção coletiva.
- Privacidade e proteção dos dados dos leitores.
- Software livre e padrões abertos.
- Interoperabilidade e sustentabilidade tecnológica.

## Estado do projeto

A iniciativa está em fase inicial de concepção e organização. A base documental
e o processo de participação estão sendo construídos; ainda não há software em
operação.

As decisões sobre arquitetura, funcionalidades, tecnologias e governança estão
abertas à discussão comunitária e podem ser revistas. O
[roadmap](docs/ROADMAP.md) descreve as etapas previstas, da fundação comunitária
ao piloto com bibliotecas participantes. Nenhuma decisão técnica deve ser
considerada consolidada antes da discussão pública.

## Stack

A arquitetura ainda não define uma stack definitiva. A avaliação deverá
priorizar:

- **ActivityPub**, ActivityStreams e padrões abertos para a comunicação
  federada.
- **BookWyrm** como alternativa ao desenvolvimento de uma rede social própria de
  leitura.
- **Sistemas de gestão bibliotecária existentes:** avaliação de soluções já
  disponíveis e adotadas por bibliotecas antes de considerar o desenvolvimento
  de um sistema próprio.
- **Formatos bibliográficos abertos** para importação, exportação e
  interoperabilidade.
- **Implantação independente, compartilhada ou comunitária**, conforme os
  recursos de cada biblioteca.
- **AGPL-3.0** como licença do software.

## Documentação

| Documento | Conteúdo |
| --- | --- |
| [Visão da iniciativa](docs/VISION.md) | Propósito, problema, públicos, capacidades e limites. |
| [Arquitetura de referência](docs/ARCHITECTURE.md) | Princípios, camadas, implantação, dados, segurança e operação. |
| [Ecossistema e integrações](docs/ECOSYSTEM.md) | Sistemas bibliotecários, BookWyrm, ActivityPub e critérios de integração. |
| [Roadmap](docs/ROADMAP.md) | Etapas de evolução, prioridades e critérios de progresso. |
| [Privacidade e proteção de dados](docs/PRIVACY.md) | Categorias de dados, consentimento, retenção, segurança e LGPD. |

## Governança e comunidade

| Documento | Conteúdo |
| --- | --- |
| [Carta de Fundação](governance/CHARTER.md) | Origem, valores e princípios fundamentais da iniciativa. |
| [Modelo de Governança](governance/GOVERNANCE.md) | Papéis, processos e tomada de decisão coletiva. |
| [Guia de Contribuição](governance/CONTRIBUTING.md) | Formas de participar e padrões para contribuições. |
| [Código de Conduta](governance/CODE_OF_CONDUCT.md) | Regras de convivência e acolhimento na comunidade. |
| [Política de Marca e Identidade](governance/TRADEMARK_POLICY.md) | Separação entre o software e a identidade institucional. |

## Como contribuir

A participação não está restrita a pessoas desenvolvedoras. Bibliotecários,
leitores, pesquisadores, coletivos culturais, organizações comunitárias e demais
interessados são parte fundamental dessa construção.

Você pode contribuir com biblioteconomia e organização de acervos,
desenvolvimento de software, arquitetura e infraestrutura tecnológica,
integração com o Fediverso, mediação cultural, documentação, comunicação e
governança.

Antes de começar, leia o [Guia de Contribuição](governance/CONTRIBUTING.md) e o
[Código de Conduta](governance/CODE_OF_CONDUCT.md). Mudanças relevantes devem
ser discutidas publicamente antes da implementação.

## Licença

O software será distribuído sob a
**GNU Affero General Public License v3.0 (AGPL-3.0)**. O texto completo da
licença está disponível no arquivo [LICENSE](LICENSE).

A licença do software não transfere direitos sobre o nome, a marca ou a
identidade institucional do projeto. Esses elementos são tratados pela
[Política de Marca e Identidade](governance/TRADEMARK_POLICY.md).
