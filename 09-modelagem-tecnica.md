# Modelagem Técnica

## Diagrama de Casos de Uso (UML)

![Diagrama de casos de uso da aplicação](_imagens/UML.png)
Fonte: Autores.

A modelagem do sistema segue a notação UML padrão [@bezerra2015]. O ecossistema mapeia as interações entre os seguintes atores e suas ações:

- **Fornecedor:** Realiza Cadastro/*Login*, cadastra Resíduos Orgânicos, define Preços, acompanha Status e recebe Pagamentos.
- **Produtor (Comprador):** Realiza Cadastro/*Login*, Busca Produtos, efetua Compras e acompanha Entregas com Rastreabilidade.
- **Operador Logístico:** Cadastra Veículos, Aceita Coletas/Entregas, Otimiza Rotas e atualiza Status de movimentação.
- **Administrador:** Valida Fornecedores, Gerencia Certificados, monitora Indicadores e resolve Disputas.
- **Sistema de Pagamento:** Interage diretamente com os casos de uso de Pagamento iniciados pelo Fornecedor e pelo Produtor.
