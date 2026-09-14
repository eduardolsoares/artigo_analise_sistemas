# Requisitos do Sistema

## Requisitos Funcionais

Os requisitos funcionais descrevem as funcionalidades que o sistema deve oferecer aos seus usuários.

### Loja

| ID | Descrição |
|:--:|:----------|
| RF01 | O sistema deve permitir que a loja cadastre os produtos (ração ou adubo) no catálogo, incluindo nome, descrição, categoria, preço, quantidade em estoque, lote e fotos. |

### Produtor (Comprador)

| ID | Descrição |
|:--:|:----------|
| RF02 | O sistema deve permitir que o produtor crie uma conta usando e-mail, CPF/CNPJ e telefone. |
| RF03 | O sistema deve permitir a busca de produtos (ração ou adubo) por tipo, composição, origem, região de produção e faixa de preço. |
| RF04 | O sistema deve permitir adicionar, remover e alterar a quantidade de itens no carrinho, incluindo pedidos fracionados. |
| RF05 | O sistema deve permitir concluir a compra dos itens do carrinho, consolidando valores (itens + frete) e gerando um novo pedido. |
| RF06 | O sistema deve oferecer opções de pagamento via cartão de crédito ou débito, com integração ao gateway financeiro. |
| RF07 | O sistema deve oferecer pagamento via PIX, gerando QR Code e chave "Copia e Cola" para compensação instantânea. |
| RF08 | O sistema deve oferecer pagamento via boleto bancário, gerando linha digitável e registrando a compra como "Aguardando Pagamento". |
| RF09 | O sistema deve calcular o frete da entrega de acordo com o CEP informado, retornando custo e prazo estimado. |
| RF10 | O sistema deve exibir em tempo real o *status* do pedido (Pendente, Em Produção, Em Separação, Saiu para Entrega, Entregue). |
| RF11 | O sistema deve possibilitar o rastreamento da entrega do produto pelo cliente. |
| RF12 | O sistema deve notificar o cliente a cada mudança no status de entrega do produto (E-mail / WhatsApp / SMS). |

### Administrador

| ID | Descrição |
|:--:|:----------|
| RF13 | O administrador deve poder visualizar as vendas realizadas, com dados do comprador, valor total, método de pagamento e data. |
| RF14 | O administrador deve poder validar e certificar os produtos cadastrados pela loja antes de publicá-los na plataforma. |
| RF15 | O administrador deve poder gerenciar disputas entre a loja e os compradores. |
| RF16 | O sistema deve manter um registro das compras realizadas pelo produtor, incluindo relatórios de rastreabilidade dos produtos. |
| RF17 | O sistema deve permitir que o produtor avalie os produtos adquiridos, com nota e parecer descritivo. |

## Requisitos Não Funcionais

Os requisitos não funcionais definem as restrições e qualidades do sistema.

| ID | Categoria | Descrição |
|:--:|:---------:|:----------|
| RNF01 | Segurança | O sistema deve estar em conformidade com a LGPD, garantindo a criptografia de dados pessoais e financeiros dos compradores. |
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

- A loja possui estrutura para registrar e manter o catálogo de produtos atualizado na plataforma.
- Os produtores rurais (compradores) possuem conectividade adequada para acessar o aplicativo, mesmo em áreas rurais com sinal limitado.
- Os serviços de entrega e frete são providos por transportadoras e serviços integrados à plataforma.
- Os serviços terceiros (Stripe para pagamentos, Google Maps para geolocalização) manterão suas APIs disponíveis e estáveis durante todo o ciclo de vida do projeto.
- A equipe de desenvolvimento estará dedicada em tempo integral durante os *sprints* planejados.