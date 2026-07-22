# Testes Funcionais

<details>
  <summary>Atividade Avaliativa</summary>

Dado um sistema fictício, os alunos deverão analisar suas funcionalidades e indicar:
- Quais testes seriam unitários
- Quais testes seriam de integração
- Quais testes seriam de sistema
- Quais testes seriam de aceitação

Justificar escolhas com base no objetivo e no nível do teste

</details>

## Sistema Fictício - Sistema de Gerenciamento de Pedidos (SGP)
O SGP é uma aplicação web utilizada por clientes e administradores para realizar e gerenciar pedidos de produtos online.

| Integrações | Funcionalidades principais | Regras de negócio |
| --- | --- | --- |
| - Integração com banco de dados de produtos<br>- Integração com serviço de autenticação<br>- Integração com serviço de pedidos | - Cadastro e autenticação de usuários<br>- Consulta de produtos disponíveis<br>- Adição e remoção de itens no carrinho <br>- Cálculo automático do valor total do pedido<br>- Finalização do pedido com confirmação | - O pedido deve conter pelo menos um item<br>- O valor total deve considerar quantidade e preço dos produtos<br>- Usuários não autenticados não podem finalizar pedidos<br>- Após a confirmação, o pedido não pode ser alterado |

###

<div align="center">

### :bar_chart: Tabela
</div>

| Funcionalidade/Regra | Tipo de Teste | Justificativa |
| --- | --- | --- |
| Cadastro de usuário| Unitário | Testa as regras internas da classe ou do método (validação de e‑mail, senha e campos obrigatórios)|
| Autenticação de usuário | Integração | Verifica a comunicação entre a aplicação e o serviço de autenticação mencionado nas integrações. |
| Consulta de produtos disponíveis | Integração |  Testa a consulta ao banco de dados de produtos. |
| Adicionar e/ou remover item ao carrinho | Unitário | Testa a lógica de adicionar um item, atualizar quantidade, validar estoque e a lógica de remoção e atualização do carrinho |
| Cálculo automático do valor total | Unitário | É uma regra de negócio implementada em um método, calculando quantidade × preço dos itens. |
| Finalização do pedido | Sistema | Exercita o fluxo completo: autenticação, carrinho, cálculo, integração com serviço de pedidos e confirmação. |
| Integração com banco de dados de produtos | Integração | Verifica a comunicação entre aplicação e banco de dados. |
| Integração com serviço de autenticação | Integração | Testa a troca de informações entre a aplicação e o serviço externo de login. |
| Integração com serviço de pedidos | Integração | Garante que os pedidos sejam enviados corretamente ao serviço responsável. |
| Pedido deve conter pelo menos um item | Unitário | Valida a regra de que o pedido não pode ficar vazio. |
| Valor total deve considerar quantidade e preço | Unitário | Verifica apenas a lógica do cálculo. |
| Usuário não autenticado não pode finalizar pedido | Sistema | Depende do funcionamento conjunto da autenticação e da funcionalidade de fechamento do pedido. |
| Após a confirmação, o pedido não pode ser alterado | Sistema | Verifica o comportamento do sistema após a conclusão do processo completo do pedido. |

### Sobre os testes
#### 1. Testes Unitários
- validar pequenas unidades de código (funções, métodos ou classes) isoladamente.

#### 2. Testes de Integração
- verificar a comunicação entre módulos internos ou sistemas externos.

#### 3. Testes de Sistema
-  validar o funcionamento completo da aplicação integrada, simulando o uso real.

####  4. Testes de Aceitação
- confirmar que o sistema atende aos requisitos e às expectativas do cliente ou usuário final.

---

<div align="center">

  Quarta-feira, dia 22 de Julho de 2026
</div>
