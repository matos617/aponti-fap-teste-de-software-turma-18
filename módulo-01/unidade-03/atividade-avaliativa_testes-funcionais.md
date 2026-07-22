# Testes Funcionais

<details>
  <summary>Atividade Avaliativa</summary>

Dado um sistema fictício, os alunos deverão analisar suas funcionalidades e indicar:
- Quais testes seriam unitários
- Quais testes seriam de integração
- Quais testes seriam de sistema
- Quais testes seriam de aceitação
Justificar escolhas com base no objetivo e no nível do teste

## Sistema Fictício - Sistema de Gerenciamento de Pedidos (SGP)
O SGP é uma aplicação web utilizada por clientes e administradores para realizar e gerenciar pedidos de produtos online.

| Integrações | Funcionalidades principais | Regras de negócio |
| --- | --- | --- |
| - Integração com banco de dados de produtos | - Cadastro e autenticação de usuários | - O pedido deve conter pelo menos um item |
| - Integração com serviço de autenticação | - Consulta de produtos disponíveis | - O valor total deve considerar quantidade e preço dos produtos |
| - Integração com serviço de pedidos | - Adição e remoção de itens no carrinho | - Usuários não autenticados não podem finalizar pedidos |
|   | - Cálculo automático do valor total do pedido | - Após a confirmação, o pedido não pode ser alterado |
|   | - Finalização do pedido com confirmação |   |
</details>

