# Avaliação de Riscos Técnicos e Mitigação

| Risco Identificado | Impacto | Estratégia de Mitigação | Justificativa |
|:------------------:|:-------:|:------------------------|:--------------|
| Vazamento de Dados Pessoais e Financeiros | Crítico | Criptografia AES-256 em repouso e controle de acesso baseado em funções (RBAC). | Expõe dados sensíveis da loja e dos compradores, violando diretamente a LGPD e gerando multas severas e processos jurídicos. |
| Sobrecarga em Épocas de Safra | Alto | Configuração de *Auto-scaling* na AWS e uso de *Load Balancer* para distribuição equilibrada de carga. | Derruba o sistema em picos de acesso coincidentes com colheitas e períodos de alta demanda por ração e adubo, interrompendo vendas e entregas. |
| Contaminação ou Qualidade dos Produtos | Alto | Exigência de certificados de qualidade dos lotes, validação obrigatória pelo administrador (RF18) e sistema de denúncias. | Produtos contaminados podem ser impróprios para uso animal ou agrícola, causando danos ambientais e responsabilidade legal. |
| Falha no *Gateway* de Pagamento | Alto | Uso do padrão *Circuit Breaker* para evitar o travamento do sistema e suporte a múltiplos provedores redundantes. | Impede a finalização dos *checkouts* e pagamentos dos compradores, paralisando o faturamento e a confiança na plataforma. |
| Indisponibilidade de Produtos na Região | Médio | Geolocalização com PostGIS para mapeamento dinâmico de produtos e notificações proativas para manter a rede ativa. | Se a oferta de produtos cai em uma região, o custo de entrega aumenta e a plataforma perde competitividade. |
