# Requisitos do Sistema

## Requisitos Funcionais

Os requisitos funcionais descrevem as funcionalidades que o sistema deve oferecer aos seus usuários.

### Fornecedor

| ID | Descrição |
|:--:|:----------|
| RF01 | O sistema deve permitir que o fornecedor crie uma conta usando e-mail, CNPJ e telefone, ou através de redes sociais. |
| RF02 | O sistema deve permitir que o fornecedor cadastre resíduos orgânicos disponíveis para destinação, incluindo fotos, descrição, tipo (alimentício, agrícola, urbano), quantidade estimada em toneladas e certificados de qualidade. |
| RF03 | O sistema deve permitir que o fornecedor defina preços por tonelada ou solicite doação para fins sociais. |
| RF04 | O sistema deve exibir em tempo real o *status* do resíduo listado (Disponível, Reservado, Em Coleta, Coletado). |
| RF05 | O sistema deve realizar pagamentos automaticamente ao fornecedor por tonelada de resíduo efetivamente coletada e processada. |
| RF06 | O sistema deve manter um histórico completo de todas as destinações de resíduos realizadas pelo fornecedor. |

### Produtor (Comprador)

| ID | Descrição |
|:--:|:----------|
| RF07 | O sistema deve permitir que o produtor crie uma conta usando e-mail, CPF/CNPJ e telefone. |
| RF08 | O sistema deve permitir a busca de produtos (ração ou adubo) por tipo, composição, origem dos resíduos, região de produção e faixa de preço. |
| RF09 | O sistema deve permitir adicionar, remover e alterar a quantidade de itens no carrinho, incluindo pedidos fracionados. |
| RF10 | O sistema deve oferecer opções de pagamento via PIX, Cartão de Crédito, Cartão de Débito e boleto bancário para grandes volumes. |
| RF11 | O sistema deve exibir em tempo real o *status* do pedido (Pendente, Em Produção, Em Separação, Saiu para Entrega, Entregue). |
| RF12 | O sistema deve manter um registro de todas as compras realizadas pelo produtor, incluindo relatórios de rastreabilidade da origem dos resíduos. |

### Logística

| ID | Descrição |
|:--:|:----------|
| RF13 | O sistema deve permitir que o operador logístico cadastre veículos, capacidades de carga e áreas de atuação. |
| RF14 | O sistema deve permitir que o operador logístico visualize coletas e entregas disponíveis e as aceite com base em proximidade e capacidade do veículo. |
| RF15 | O sistema deve integrar mapas para otimização de rotas de coleta e entrega, considerando peso, volume e urgência. |
| RF16 | O sistema deve permitir que o operador logístico atualize o *status* de cada etapa: coletado, em trânsito, em processamento, entregue. |

### Administrador

| ID | Descrição |
|:--:|:----------|
| RF17 | O administrador deve poder validar e certificar fornecedores e seus resíduos orgânicos antes de permitirem a publicação na plataforma. |
| RF18 | O administrador deve ter acesso a painel de indicadores: volume de resíduos processados, pedidos ativos, receita da plataforma e métricas de sustentabilidade. |
| RF19 | O administrador deve poder gerenciar disputas entre fornecedores, compradores e operadores logísticos. |

## Requisitos Não Funcionais

Os requisitos não funcionais definem as restrições e qualidades do sistema.

| ID | Categoria | Descrição |
|:--:|:---------:|:----------|
| RNF01 | Segurança | O sistema deve estar em conformidade com a LGPD, garantindo a criptografia de dados pessoais e financeiros dos fornecedores e compradores. |
| RNF02 | Desempenho | O tempo de resposta para buscas de produtos não deve exceder 2 segundos sob carga normal. |
| RNF03 | Disponibilidade | O sistema deve estar disponível 99,9% do tempo. |
| RNF04 | Usabilidade | A interface deve ser acessível e seguir os padrões de *Design System* (iOS, Android e Web). |
| RNF05 | Escalabilidade | A infraestrutura deve suportar um aumento repentino de acessos (ex: safra agrícola) sem perda de *performance*. |
| RNF06 | Rastreabilidade | O sistema deve garantir rastreabilidade completa da origem dos resíduos até o produto final (ração ou adubo), atendendo a requisitos da legislação ambiental. |

## Restrições e Premissas

### Restrições

- **Técnicas:** O *app* deve ser compatível com iOS 14+ e Android 8+ como versões mínimas. O sistema deve operar em infraestrutura em nuvem (AWS).
- **Legais:** O sistema deve estar em conformidade com a LGPD (Lei nº 13.709/2018), com a Política Nacional de Resíduos Sólidos (Lei nº 12.305/2010) e com as normas do CONAMA para destinação de resíduos orgânicos.
- **De negócio:** O escopo do MVP limita-se às funcionalidades classificadas como *Must Have*, com expansões previstas apenas para versões pós-lançamento.
- **De plataforma:** Os aplicativos mobile devem ser publicados obrigatoriamente na App Store (iOS) e Google Play (Android). O painel administrativo deve ser acessível via navegador web moderno.

### Premissas

- Os fornecedores (restaurantes, fazendas, indústrias de alimentos) possuem *smartphones* ou computadores com acesso à internet para operar a plataforma.
- Os produtores rurais (compradores) possuem conectividade adequada para acessar o aplicativo, mesmo em áreas rurais com sinal limitado.
- Os operadores logísticos dispõem de veículos adequados para transporte de resíduos orgânicos e produtos acabados (ração e adubo).
- Os serviços terceiros (Stripe para pagamentos, Google Maps para geolocalização) manterão suas APIs disponíveis e estáveis durante todo o ciclo de vida do projeto.
- A equipe de desenvolvimento estará dedicada em tempo integral durante os *sprints* planejados.
