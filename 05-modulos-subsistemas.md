# Divisão em Módulos e Subsistemas

O sistema é dividido em quatro módulos independentes que se comunicam via APIs REST, seguindo as boas práticas de arquitetura de software [@sommerville2018].

## Módulo da Loja

*Painel Web* (React.js)

- RF01, Cadastro de produtos (ração/adubo) no catálogo (nome, descrição, categoria, preço, estoque, lote, fotos)

## Módulo do Produtor (Comprador)

*App* Mobile (React Native / Expo)

- RF02, Cadastro e *login* de produtores rurais (CPF/CNPJ)
- RF03, Busca e filtragem de produtos por tipo (ração/adubo), composição, origem e região
- RF04, Carrinho de compras com pedidos fracionados
- RF05, *Checkout* e compra dos itens do carrinho
- RF06, Pagamento via cartão de crédito ou débito
- RF07, Pagamento via PIX
- RF08, Pagamento via boleto bancário
- RF09, Cálculo de frete por CEP
- RF10, *Status* do pedido em tempo real
- RF11, Rastreamento de pedidos
- RF12, Notificações de entrega (E-mail / WhatsApp / SMS)

## Core Backend

API & Orquestração (Node.js)

- Autenticação JWT e controle RBAC por perfil (Loja, Produtor, Administrador)
- Processamento de pagamentos (Stripe/PIX/boleto)
- Integração com *gateways* de terceiros (geolocalização, notificações)
- Banco de dados centralizado (PostgreSQL com PostGIS)
- Motor de rastreabilidade de resíduos (origem → processamento → produto final)
