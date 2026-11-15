# Ecossistema e Integrações

**Versão:** 0.1 — Documento inicial  
**Status:** Em discussão comunitária

## 1. Objetivo

Este documento descreve o ecossistema tecnológico e comunitário no qual a iniciativa pretende atuar.

A proposta é integrar sistemas de gestão bibliotecária, plataformas sociais de leitura e protocolos de comunicação federada, evitando reinventar soluções que já existem e preservando a autonomia das instituições participantes.

A arquitetura definitiva ainda não está estabelecida. Este documento apresenta os componentes considerados relevantes e as relações desejadas entre eles.

## 2. Visão geral do ecossistema

O ecossistema é composto por quatro dimensões principais:

1. Bibliotecas e seus sistemas de gestão.
2. Leitores e suas comunidades de leitura.
3. Serviços de descoberta e compartilhamento de informações.
4. Infraestrutura federada de comunicação.

Essas dimensões deverão cooperar por meio de interfaces abertas, integrações e protocolos interoperáveis.

## 3. Sistemas de gestão bibliotecária

Os sistemas de gestão bibliotecária, também conhecidos como ILS (Integrated Library Systems), são responsáveis pelas operações administrativas e bibliotecárias.

Entre suas funções estão:

- Catalogação.
- Organização de obras, edições e exemplares.
- Controle de disponibilidade.
- Empréstimos e devoluções.
- Reservas.
- Gestão de leitores.
- Relatórios e estatísticas administrativas.

A iniciativa deverá avaliar sistemas existentes antes de decidir pela criação de uma solução própria.

### 3.1. Koha

O [Koha](https://koha-community.org/) é uma das alternativas consideradas.

É um sistema de gestão bibliotecária de código aberto, utilizado por bibliotecas de diferentes portes e contextos.

Pontos relevantes:

- Possui recursos abrangentes de gestão bibliotecária.
- Oferece funcionalidades de catalogação e circulação.
- Disponibiliza interfaces de integração.
- Possui uma comunidade estabelecida.
- É desenvolvido principalmente em Perl.
- Utiliza licença GPL-3.0.

O Koha não deve ser considerado automaticamente a solução definitiva. Sua adequação deverá ser avaliada em relação à infraestrutura, aos custos de operação, à facilidade de implantação e às necessidades das bibliotecas participantes.

## 4. BookWyrm e comunidades de leitura

O [BookWyrm](https://joinbookwyrm.com/) é uma plataforma social de leitura integrada ao Fediverso.

Seu propósito é permitir que leitores compartilhem experiências relacionadas aos livros, incluindo:

- Registros de leitura.
- Resenhas.
- Avaliações.
- Listas de livros.
- Recomendações.
- Interações entre leitores.

A iniciativa pretende aproveitar esse ecossistema, em vez de desenvolver uma rede social de leitura paralela.

### 4.1. Papel do BookWyrm

O BookWyrm deverá ser considerado uma camada social de leitura.

Ele não substitui um sistema de gestão bibliotecária e não deve ser tratado como fonte autoritativa para:

- Disponibilidade de exemplares.
- Situação de empréstimos.
- Reservas.
- Políticas de circulação.
- Dados administrativos das bibliotecas.

A integração deverá respeitar os modelos de dados e as funcionalidades próprias do BookWyrm.

### 4.2. Integração com bibliotecas

A integração poderá permitir:

- Divulgação de obras disponíveis.
- Compartilhamento de listas temáticas.
- Descoberta de resenhas públicas.
- Divulgação de clubes de leitura.
- Conexão entre leitores e bibliotecas.
- Publicação voluntária de experiências de leitura.

A disponibilidade técnica dessas funcionalidades dependerá das interfaces e dos mecanismos de interoperabilidade oferecidos pelo BookWyrm.

Não se deve presumir que qualquer resenha ou avaliação possa ser consultada diretamente por qualquer sistema de gestão bibliotecária. A descoberta, a ingestão e a apresentação desses dados dependerão da compatibilidade técnica, das interfaces disponíveis e das condições de uso.

## 5. ActivityPub e Fediverso

O [ActivityPub](https://www.w3.org/TR/activitypub/) é um protocolo aberto de comunicação federada, publicado como recomendação do W3C.

Ele permite que diferentes servidores e plataformas troquem atividades e interajam sem depender de um serviço central.

A iniciativa pretende utilizar o ActivityPub como mecanismo de interoperabilidade social e comunicação entre participantes.

### 5.1. Possíveis aplicações

- Perfis públicos de bibliotecas.
- Divulgação de eventos.
- Publicação de novidades e aquisições.
- Compartilhamento de listas públicas.
- Comunicação com leitores e organizações.
- Integração com outras instâncias do Fediverso.

### 5.2. Limites do protocolo

O ActivityPub não define, sozinho, todas as regras de funcionamento de um sistema bibliotecário.

O protocolo permite a troca de atividades, mas não estabelece um modelo universal para catalogação, empréstimos, reservas ou circulação de exemplares.

Além disso, plataformas como o BookWyrm possuem modelos de dados e tipos de atividade próprios.

Por isso, a integração deverá considerar:

- Compatibilidade entre implementações.
- Tipos de atividade reconhecidos.
- Identificadores de objetos.
- Políticas de distribuição e privacidade.
- Tratamento de atualizações e exclusões.
- Limites de cada plataforma.

## 6. Identificação bibliográfica

A interoperabilidade bibliográfica exige cuidado com a identificação de obras e edições.

Uma mesma obra pode possuir diferentes edições, traduções, formatos e publicações.

O ISBN identifica uma edição ou publicação específica, não necessariamente a obra intelectual em sentido amplo.

A integração deverá evitar que registros de edições diferentes sejam tratados como se fossem o mesmo exemplar ou a mesma publicação.

Sempre que possível, deverão ser considerados:

- ISBN-10 e ISBN-13.
- Título e subtítulo.
- Autoria.
- Editora.
- Ano de publicação.
- Idioma.
- Formato.
- Identificadores bibliográficos externos.
- Relação entre obra, edição e exemplar.

A adoção de padrões bibliográficos deverá ser avaliada com a participação de profissionais de biblioteconomia.

## 7. Camada de integração

Uma possibilidade arquitetural é utilizar uma camada intermediária responsável por conectar os sistemas de gestão bibliotecária ao Fediverso e às plataformas sociais de leitura.

Essa camada poderá assumir responsabilidades como:

- Adaptar formatos de dados.
- Sincronizar informações selecionadas.
- Publicar atividades federadas.
- Consumir atividades externas.
- Controlar permissões e políticas de publicação.
- Registrar falhas de integração.
- Evitar duplicidade de eventos.
- Gerenciar identificadores externos.

Essa camada não deverá se tornar proprietária dos dados das bibliotecas nem impor uma plataforma única.

Sua necessidade, responsabilidades e limites serão definidos durante a avaliação arquitetural.

## 8. Autonomia das bibliotecas

Cada biblioteca deverá manter autonomia sobre:

- Seu acervo.
- Seus exemplares.
- Seus leitores.
- Suas políticas de empréstimo.
- Seus prazos e regras de circulação.
- Seus dados administrativos.
- Sua presença pública na rede.

A participação no ecossistema não deverá exigir a publicação integral do catálogo nem a exposição de informações administrativas.

Cada instituição poderá decidir quais informações deseja compartilhar.

## 9. Cooperação entre bibliotecas

A visão de longo prazo contempla a possibilidade de cooperação entre bibliotecas.

Entre as possibilidades a serem estudadas estão:

- Compartilhamento de registros bibliográficos.
- Descoberta de acervos de outras instituições.
- Intercâmbio de informações sobre coleções.
- Apoio à catalogação.
- Divulgação de materiais disponíveis em outras bibliotecas.
- Cooperação em atividades culturais.

A circulação física de exemplares entre bibliotecas envolve responsabilidades administrativas, logísticas e jurídicas. Portanto, não deve ser presumida como consequência automática da federação tecnológica.

## 10. Privacidade e publicação de informações

A integração entre sistemas deverá respeitar a privacidade dos leitores.

Não deverão ser publicados automaticamente:

- Históricos de empréstimos.
- Reservas.
- Dados cadastrais.
- Informações de contato.
- Hábitos de leitura.
- Informações administrativas internas.

A publicação de resenhas, avaliações e atividades de leitura deverá depender da escolha do leitor e das funcionalidades disponíveis na plataforma utilizada.

## 11. Critérios para avaliação de integrações

Toda integração deverá ser avaliada considerando:

1. Compatibilidade com protocolos abertos.
2. Maturidade e continuidade do projeto integrado.
3. Licença e condições de uso.
4. Disponibilidade de documentação.
5. Segurança e privacidade.
6. Custos de implantação e manutenção.
7. Facilidade de operação pelas bibliotecas.
8. Autonomia das instituições.
9. Qualidade da interoperabilidade.
10. Possibilidade de substituição futura do componente.

## 12. Decisões ainda abertas

Permanecem em discussão:

- A adoção ou não do Koha como sistema de referência.
- A possibilidade de integração com outros sistemas bibliotecários.
- A necessidade de uma camada intermediária própria.
- A estratégia de integração com o BookWyrm.
- A existência de perfis federados próprios para bibliotecas.
- O modelo de hospedagem e distribuição das instâncias.
- O compartilhamento de catálogos.
- A eventual cooperação para circulação de exemplares.

Nenhuma dessas decisões deverá ser considerada definitiva antes de avaliação técnica e discussão comunitária.