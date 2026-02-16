## Desafio — Modelagem de Dados em Grafo para Serviço de Streaming

Neste desafio foi proposto o desenvolvimento de um modelo de banco de dados orientado a grafos para um serviço de streaming de filmes e séries, utilizando conceitos de modelagem de grafos aplicados ao contexto de recomendação baseada em relacionamentos.

O objetivo principal foi representar entidades do domínio de streaming como nós e suas interações como relacionamentos, priorizando conexões semânticas entre os dados ao invés de uma estrutura relacional tradicional.

---

### Entidades Modeladas (Nós)

Foram definidos os seguintes tipos de nós:

- **User** — representa usuários da plataforma  
- **Movie** — representa filmes disponíveis  
- **Series** — representa séries  
- **Actor** — representa atores  
- **Director** — representa diretores  
- **Genre** — representa gêneros de conteúdo  

Cada nó possui propriedades relevantes, como identificadores únicos e atributos descritivos (exemplo: nome, título, ano, email, etc.).

---

### Relacionamentos Criados

Foram implementadas as seguintes conexões entre entidades:

- **WATCHED** — conecta `User → Movie`, contendo a propriedade `rating`  
- **ACTED_IN** — conecta `Actor → Movie`  
- **DIRECTED** — conecta `Director → Movie`  
- **IN_GENRE** — conecta `Movie → Genre`  

Esses relacionamentos permitem representar o comportamento do usuário e as características estruturais do conteúdo, possibilitando análises e recomendações mais eficientes.

---

### Ferramentas Utilizadas

- **Arrows.app** — para criação do diagrama visual do grafo  
- **Neo4j / Cypher (conceitual)** — para futura implementação no banco de grafos  

---

### Objetivo Arquitetural

A modelagem foi construída com foco em:

- Recomendação baseada em comportamento do usuário  
- Navegação eficiente entre entidades relacionadas  
- Escalabilidade para análise de conexões complexas  
- Facilidade de evolução do modelo sem necessidade de reestruturação completa  

---

### Resultado

O resultado foi um grafo funcional representando interações entre usuários e conteúdos, adequado para cenários de recomendação, análise comportamental e consultas semânticas complexas.
