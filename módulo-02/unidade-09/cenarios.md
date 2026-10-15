# Cenários de automação: Practice Software Testing (Toolshop)

## 1. Sistema escolhido
- **Sistema:** [Practice Software Testing - ToolShop](https://practicesoftwaretesting.com)
- **O que faz:** loja online de ferramentas feita para praticar testes.
- **Critérios usados para decidir:** Estabilidade, velocidade, frequência de uso, importância das funcionalidades e facilidade de automatização.

## 2. Cenários

| # | Cenário | Decisão | Justificativa |
|---|---------|---------|---------------|
| 1 | Login com usuário válido | Manual | Login com usuário válido para saber se o sistema entra corretamenge com a conta logada |
| 2 | Compra de produto | Automatizar | Etapa para verificar se o ciclo de compra dos produtos ocorre normalmente, verificando se todos os produtos respondem a compra |
| 3 | Uso do filtro por categoria | Automatizar | Usar cada rótulo de categoria no filtro para encontrar os produtos certos |
| 4 | Uso do filtro por preço | Automatizar | Filtrar por preço/valor e ter como resposta os produtos que correspondem á média de valor/entre os valores escolhidos |
| 5 | Pesquisa do produto por nome | Automatizar | Checar com automação se todos os produtos disponíveis correspondem ao pesquisar seu nome ou palavras-chaves  |
| 6 | Adicionar produto ao carrinho | Automatizar | Pode ser testada repetidamente para verificar se os produtos são adicionados corretamente |
| 7 | Remover produto do carrinho | Manual | Explorar diferentes situações, como remover o único produto ou retirar um item de um carrinho com vários produtos. |
| 8 | Cadastro de novo usuário | Manual | Permitir manualmente explorar campos obrigatórios, dados inválidos e mensagens de erro, avaliando também a clareza das orientações apresentadas ao usuário durante o cadastro |

## 3. Pirâmide de testes

| Nível | Tipo de teste | Quantidade | Exemplo de cenário |
|-------|---------------|-----------|--------------------|
| Topo | E2E / UI | Poucos | ... |
| Meio | Integração / API | Alguns | ... |
| Base | Unitário | Muitos | ... |

## 4. Conclusão
