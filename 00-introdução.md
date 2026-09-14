# Introdução {-}

O ReFeed.inc é uma plataforma de e-commerce inovadora desenvolvida para reaproveitar resíduos orgânicos, como restos de alimentação, cascas de frutas, podas de jardim e subprodutos agroindustriais, transformando-os em ração animal e adubo orgânico de qualidade, seguindo as melhores práticas de engenharia de software [@sommerville2018]. O projeto foca em resolver o desperdício massivo de resíduos orgânicos no Brasil, oferecendo uma solução tecnológica que conecta quem tem resíduos orgânicos disponíveis a quem pode transformá-los em produtos de alto valor agrícola e pecuário.

Diferentemente de iniciativas anteriores como a Planta Feliz Adubo, que se restringe à produção de adubo orgânico, o ReFeed.inc amplia o escopo ao oferecer também ração animal derivada de resíduos orgânicos processados, criando um ecossistema completo de economia circular.

A arquitetura do sistema foi estruturada para atender às necessidades específicas de três pilares:

- **Para o Fornecedor:** Oferece uma jornada de cadastro de resíduos simplificada, que abrange desde o registro de conta (RF01) e listagem de resíduos orgânicos com fotos e descrições detalhadas (RF02), até o acompanhamento do destino dos resíduos fornecidos (RF06) e o recebimento de pagamentos por tonelada processada (RF05).

- **Para o Produtor (Comprador):** Provê uma experiência de compra fluida, permitindo busca inteligente por tipo de produto, ração ou adubo, e pelas características dos resíduos de origem (RF03), carrinho de compras e checkout (RF04), além de rastreamento de entregas de grandes volumes (RF07).

- **Para a Logística:** Disponibiliza uma interface de gerenciamento de coletas e entregas baseada em geolocalização (RF10), com otimização de rotas para veículos de grande porte e rastreamento em tempo real das remessas (RF11).

Como estratégia de mercado, o desenvolvimento do ReFeed.inc prioriza um MVP (Mínimo Produto Viável) focado na funcionalidade principal de conexão entre fornecedores e compradores com segurança e rastreabilidade (*Must Have*). Isso inclui a implementação imediata da conformidade com a LGPD (RNF01) e do sistema de upload de certificados de qualidade dos resíduos (RF02), garantindo que a base do produto seja viável, segura e escalável antes da expansão para recursos avançados, como otimização por IA ou marketplace de insumos agrícolas.
