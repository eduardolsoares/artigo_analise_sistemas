# Plano de Implementação

## *Sprints*

### *Sprint* 1 (01/05 – 14/05)

- **Esforço:** Moderado
- **Responsáveis:** Kayla, Eduardo Leite Soares
- **Descrição:** Codificação das interfaces dos aplicativos para iOS e Android (fornecedor e comprador) e painel de controle administrativo e logístico. Definição de regras de negócio iniciais.
- **Justificativa:** Foca no desenvolvimento visual (*front-end*) e regras iniciais de aplicativo e painéis, o que exige volume de código, mas lida com menor complexidade estrutural de infraestrutura neste momento.

### *Sprint* 2 (14/05 – 21/05)

- **Esforço:** Alto
- **Responsáveis:** João Gabriel Amaral, Lucas de Moraes, Arthur Martins de Andrade
- **Descrição:** Modelagem do banco de dados com PostGIS para consultas geoespaciais. Aferição da integridade da arquitetura escolhida. Criação dos microsserviços (Auth, Order, Catalog, Logistics, Traceability) e integração deles ao banco.
- **Justificativa:** Criação do alicerce do sistema. Envolve modelagem de dados complexa com rastreabilidade, microsserviços, *cache* e validação de uma arquitetura que precisa suportar todo o projeto.

### *Sprint* 3 (21/05 – 28/05)

- **Esforço:** Alto
- **Responsáveis:** Lucas de Moraes, Kayla, João Gabriel Amaral
- **Descrição:** Construção das APIs REST. Implementação do motor de rastreabilidade de resíduos (origem → processamento → produto final).
- **Justificativa:** Desenvolvimento de APIs e integração com múltiplos sistemas externos críticos (pagamento, mapas e rastreabilidade), exigindo alta complexidade de comunicação e tratamento de erros.

### *Sprint* 4 (28/05 – 14/06)

- **Esforço:** Moderado
- **Responsáveis:** Eduardo Leite Soares, Kayla
- **Descrição:** Conexão com sistemas externos (*gateway* de pagamento, mapas para geolocalização e sistemas de gestão dos parceiros logísticos). Integração com Stripe para pagamentos e Google Maps para otimização de rotas.
- **Justificativa:** Fase voltada para a integração com parceiros externos e garantia de qualidade, validação e segurança (testes e *checklists*) sobre o código que já foi desenvolvido nas etapas anteriores.

### *Sprint* 5 (01/06 – 14/06)

- **Esforço:** Alto
- **Responsáveis:** João Gabriel Amaral, Lucas de Moraes, Arthur Martins de Andrade
- **Descrição:** Bateria de testes. *Checklist* de segurança da aplicação. Testes de rastreabilidade e integração com a base de dados geoespacial. Preparos pré-produção. Preparação da infraestrutura.
- **Justificativa:** Configuração final e *deploy*. Preparar a infraestrutura de pré-produção e produção exige rigor técnico absoluto para garantir que o sistema funcione com estabilidade e segurança no lançamento.

## Estratégias de Acompanhamento

- *Daily Scrum* para inspecionar diariamente o progresso no desenvolvimento do sistema
- *Reports* a cada *daily* que resumem o que precisa ser feito, garantindo coesão da equipe
- Pipelines de CI/CD para verificar as entregas realizadas pelas equipes
- Utilizar quadro Kanban como ferramenta visual para mapear as tarefas do *Sprint backlog*, promovendo transparência quanto ao progresso das mesmas
