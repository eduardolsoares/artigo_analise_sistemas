## Diagrama de Componentes (Microserviços)

O fluxo arquitetural segue o padrão estabelecido:

Apps Mobile / Web → API Gateway (ponto único de entrada) → Microserviços → Bases de Dados

### Camada de Microserviços

- **Auth Service:** Gerencia JWT, conformidade com a LGPD e controle de acesso por perfil (Fornecedor, Produtor, Logística, Administrador).
- **Order Service:** Processa Pedidos, fluxo de Pagamento e faturamento entre fornecedores e compradores.
- **Catalog Service:** Gerencia Catálogo de Resíduos Orgânicos, produtos (ração/adubo) e Estoque.
- **Logistics Service:** Gerencia coletas, entregas, otimização de rotas e rastreamento em tempo real.
- **Traceability Service:** Responsável pela rastreabilidade completa: origem do resíduo → processamento → produto final (ração ou adubo).

![Diagrama de Componentes, Arquitetura de Microserviços do ReFeed.inc](imagens/diagrama_componentes.png){#fig-componentes}

Fonte: Autores.

### Camada de Persistência e Cache

- **PostgreSQL + PostGIS (Dados Estruturados e Geoespaciais):** Consumido pelos serviços de Autenticação (Auth), Pedidos (Order), Catálogo (Catalog) e Logística (Logistics) com consultas de proximidade e rotas.
- **Redis (Cache / Sessões):** Utilizado para otimização nos serviços de Pedidos (Order) e Catálogo (Catalog).
- **AWS S3 (Armazenamento):** Destinado à persistência de fotos de resíduos, certificados de qualidade e documentos de rastreabilidade.

A arquitetura geral do sistema segue o padrão de microsserviços, com ponto único de entrada via API Gateway distribuindo requisições entre os cinco serviços especializados e persistindo dados nas camadas de PostgreSQL, Redis e S3 conforme a necessidade de cada operação.

### Diagrama de Implantação

O ReFeed.inc é implantado em infraestrutura em nuvem (AWS). Os aplicativos *mobile* (React Native / Expo) e os painéis *web* (React.js) acessam o sistema via API Gateway, que distribuí as requisições entre os microsserviços *Node.js*. Os dados são persistidos em PostgreSQL + PostGIS e Redis, com arquivos armazenados no AWS S3. Integrações externas realizam o processamento de pagamentos (Stripe) e a geolocalização e otimização de rotas (Google Maps / Mapbox).

![Diagrama de Implantação do ReFeed.inc](imagens/diagrama_implantacao.png){#fig-implantacao}

Fonte: Autores.
