## Diagrama de Componentes (Microserviços)

O fluxo arquitetural segue o padrão estabelecido:

Apps Mobile / Web → API Gateway (ponto único de entrada) → Microserviços → Bases de Dados

### Camada de Microserviços

- **Auth Service:** Gerencia JWT, conformidade com a LGPD e controle de acesso por perfil (Fornecedor, Produtor, Logística, Administrador).
- **Order Service:** Processa Pedidos, fluxo de Pagamento e faturamento entre fornecedores e compradores.
- **Catalog Service:** Gerencia Catálogo de Resíduos Orgânicos, produtos (ração/adubo) e Estoque.
- **Logistics Service:** Gerencia coletas, entregas, otimização de rotas e rastreamento em tempo real.
- **Traceability Service:** Responsável pela rastreabilidade completa: origem do resíduo → processamento → produto final (ração ou adubo).

### Camada de Persistência e Cache

- **PostgreSQL + PostGIS (Dados Estruturados e Geoespaciais):** Consumido pelos serviços de Autenticação (Auth), Pedidos (Order), Catálogo (Catalog) e Logística (Logistics) com consultas de proximidade e rotas.
- **Redis (Cache / Sessões):** Utilizado para otimização nos serviços de Pedidos (Order) e Catálogo (Catalog).
- **AWS S3 (Armazenamento):** Destinado à persistência de fotos de resíduos, certificados de qualidade e documentos de rastreabilidade.

![Arquitetura geral do sistema ReFeed.inc.](_imagens/arquitetura.png)

Fonte: Autores.
