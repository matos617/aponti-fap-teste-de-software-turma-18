<div align="center">

# Técnicas de Teste
</div>

<details>

  <summary>Atividade Avaliativa</summary>

## Atividade Avaliativa
Na sua aplicação, crie casos de teste utilizando às técnicas aprendidas
- 3 casos de valor limite
- 3 casos de particionamento de equivalência
- Identifique 3 possíveis estados e transições

Entregar testes estruturados, contendo:
- Entradas
- Técnicas utilizadas
- Resultado esperado
</details>

---

# Casos de Teste – Funcionalidade: Perfis e Permissões

## Objetivo

Aplicar as técnicas de **Análise de Valor Limite**, **Particionamento de Equivalência** e **Estados e Transições** à funcionalidade **Perfis e Permissões**, verificando o comportamento do sistema durante o cadastro, configuração de permissões e exclusão de perfis.

---

## 1. Casos de Teste – Valor Limite
Verifica o comportamento do sistema nos limites mínimo e máximo aceitos para determinada entrada.

<br>

### CT-VL-01 – Cadastro de perfil com quantidade mínima de caracteres

| Item  | Descrição |
| --- | --- |
| **Entrada** | Nome do perfil contendo a quantidade mínima permitida de caracteres |
| **Técnica utilizada** | Análise de Valor Limite |
| **Resultado esperado** | O sistema deve aceitar o cadastro caso a quantidade mínima de caracteres seja válida |

**Exemplo:** Se o mínimo for **3 caracteres**, testar um perfil com:

`TI`

`ADM`

O valor abaixo do limite deve ser rejeitado e o valor mínimo aceito.

<br>

### CT-VL-02 – Cadastro de perfil com quantidade máxima de caracteres

| Item | Descrição |
| --- | --- |
| **Entrada**  | Nome do perfil contendo a quantidade máxima permitida de caracteres |
| **Técnica utilizada** | Análise de Valor Limite |
| **Resultado esperado** | O sistema deve aceitar o nome no limite máximo permitido e impedir valores superiores ao limite |

**Exemplo:** Se o campo permitir **50 caracteres**, testar:

* 50 caracteres;
* 51 caracteres.

<br>

### CT-VL-03 – Limite de permissões atribuídas ao perfil

| Item  | Descrição |
| --- | --- |
| **Entrada** | Perfil com a quantidade mínima e máxima possível de permissões selecionadas |
| **Técnica utilizada** | Análise de Valor Limite |
| **Resultado esperado** | O sistema deve permitir o cadastro conforme as regras de quantidade mínima ou máxima de permissões |

Exemplo de situações:

* Nenhuma permissão selecionada;
* Uma permissão selecionada;
* Todas as permissões disponíveis selecionadas.

---

## 2. Casos de Teste – Particionamento de Equivalência

A técnica de **Particionamento de Equivalência** divide as entradas em grupos que devem apresentar comportamentos semelhantes.

<br>

### CT-PE-01 – Cadastro de perfil com nome válido

| Item | Descrição |
| --- | --- |
| **Entrada** | Nome válido para um perfil, como `Médico` ou `Funcionário` |
| **Técnica utilizada** | Particionamento de Equivalência |
| **Classe de equivalência** | Entrada válida |
| **Resultado esperado** | O sistema deve permitir o cadastro do perfil com sucesso |

<br>

### CT-PE-02 – Cadastro de perfil sem nome

| Item | Descrição |
| --- | --- |
| **Entrada** | Campo de nome do perfil vazio |
| **Técnica utilizada** | Particionamento de Equivalência |
| **Classe de equivalência** | Entrada inválida |
| **Resultado esperado** | O sistema não deve permitir o cadastro e deve informar que o preenchimento do campo é obrigatório |

<br>

### CT-PE-03 – Cadastro de perfil com nome inválido

| Item | Descrição |
| --- | --- |
| **Entrada**  | Nome contendo caracteres ou informações não permitidas pelas regras do sistema |
| **Técnica utilizada** | Particionamento de Equivalência |
| **Classe de equivalência** | Entrada inválida |
| **Resultado esperado** | O sistema deve rejeitar o cadastro e informar que o valor inserido é inválido |

---

## 3. Estados e Transições

A técnica de **Estados e Transições** verifica como o sistema se comporta quando uma entidade muda de um estado para outro.

Na funcionalidade **Perfis e Permissões**, podem ser identificados os seguintes estados:

<br>

### Estado 1 – Perfil não cadastrado → Perfil cadastrado

#### Transição

**Perfil inexistente → Cadastro realizado → Perfil ativo**

| Item | Descrição |
| --- | --- |
| **Entrada/Ação** | Administrador cadastra um novo perfil com informações válidas |
| **Técnica utilizada** | Estados e Transições |
| **Resultado esperado** | O sistema deve criar o perfil e disponibilizá-lo na lista de perfis |

<br>

### Estado 2 – Perfil com acesso permitido → Permissão removida

#### Transição

**Perfil com acesso → Permissão removida → Acesso bloqueado**

| Item | Descrição |
| --- | --- |
| **Entrada/Ação** | Administrador remove a permissão de acesso do perfil a uma funcionalidade |
| **Técnica utilizada** | Estados e Transições |
| **Resultado esperado** | O usuário associado ao perfil não deve conseguir acessar a funcionalidade após a atualização das permissões |

<br>

### Estado 3 – Perfil ativo → Perfil excluído

#### Transição

**Perfil ativo → Exclusão confirmada → Perfil removido/inativo**

| Item | Descrição |
| --- | --- |
| **Entrada/Ação** | Administrador seleciona um perfil e confirma sua exclusão |
| **Técnica utilizada** | Estados e Transições |
| **Resultado esperado** | O perfil deve ser removido do sistema e o usuário associado não deve conseguir acessar o sistema utilizando suas credenciais |

---

<div align="center">
01/09/2026
</div>
