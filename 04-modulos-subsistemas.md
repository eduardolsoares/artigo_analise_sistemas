# Divisão em Módulos e Subsistemas

O sistema é dividido em quatro módulos independentes que se comunicam via APIs REST, seguindo as boas práticas de arquitetura de software [@sommerville2018].

## Módulo do Fornecedor

*App* Mobile (React Native / Expo)

- RF01, Cadastro e *login* de fornecedores (CNPJ, rede social)
- RF02, Listagem de resíduos orgânicos (fotos, descrição, tipo, quantidade, certificados)
- RF03, Definição de preços por tonelada ou opção de doação
- RF04, Acompanhamento do *status* do resíduo listado
- RF05, Recebimento de pagamentos por tonelada coletada
- RF06, Histórico completo de destinações de resíduos

## Módulo do Produtor (Comprador)

*App* Mobile (React Native / Expo)

- RF07, Cadastro e *login* de produtores rurais (CPF/CNPJ)
- RF08, Busca e filtragem de produtos por tipo (ração/adubo), composição, origem e região
- RF09, Carrinho de compras com pedidos fracionados e *checkout*
- RF10, Pagamento via PIX, Cartão, Débito e boleto bancário
- RF11, Rastreamento de pedidos em tempo real
- RF12, Histórico de compras com relatórios de rastreabilidade

## Módulo de Logística

*App* Mobile (React Native) + Painel Web (React.js)

- RF13, Cadastro de veículos, capacidades e áreas de atuação
- RF14, Visualização e aceitação de coletas/entregas disponíveis
- RF15, Otimização de rotas por peso, volume e urgência
- RF16, Atualização de *status* por etapa (coletado, em trânsito, processado, entregue)

## Core Backend

API & Orquestração (Node.js)

- Autenticação JWT e controle RBAC por perfil (Fornecedor, Produtor, Logística, Administrador)
- Processamento de pagamentos (Stripe/PIX/boleto)
- Integração com *gateways* de terceiros (geolocalização, notificações)
- Banco de dados centralizado (PostgreSQL com PostGIS)
- Motor de rastreabilidade de resíduos (origem → processamento → produto final)
