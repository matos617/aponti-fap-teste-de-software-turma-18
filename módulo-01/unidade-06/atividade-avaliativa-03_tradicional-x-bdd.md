# Tradicional x BDD

<details>

  <summary>Atividade Avaliativa</summary>

## Atividade Avaliativa
- Comparar o mesmo comportamento do sistema usando duas abordagens diferentes
- Criar um cenário BDD e um cenário Tradicional

Responder:
- Qual o formato mais fácil de escrever?
- Qual comunica melhor o comportamento?
- Qual seria mais fácil de manter?
</details>

---

## Tradicional

### ID: CT-02
### Título: Criar um novo perfil de usuário

### Pré-condição:
O administrador deve estar autenticado no sistema e acessar a funcionalidade Perfis e Permissões.

| Passo | Ação | Resultado esperado |
| --- | --- | --- |
| 1	| Acessar a funcionalidade Perfis e Permissões |	A funcionalidade deve ser exibida |
| 2	| Selecionar a opção para criar um novo perfil | O formulário de cadastro deve ser exibido |
| 3	| Preencher as informações válidas do perfil | As informações devem ser aceitas |
| 4	| Definir as permissões de acesso | As permissões devem ser registradas |
| 5	| Salvar o cadastro |	O perfil deve ser criado com sucesso e ficar disponível no sistema |

<br>

## Gherkin

```gherkin
Cenário: Cadastro de um novo perfil com sucesso

  Dado que o administrador está na funcionalidade de Perfis e Permissões
  Quando o administrador cadastra um novo perfil com informações válidas
  E define as permissões de acesso do perfil
  Então o sistema deve cadastrar o novo perfil com sucesso
  E o perfil deve ficar disponível para utilização no sistema
```

<br>

## Respostas

### Qual o formato mais fácil de escrever?
O mais fácil é o comportamental (BDD), pois ele já explica o comportamento esperado da ação do que trazer o passo a passo detalhado e cheio sobre onde clicar.

### Qual comunica melhor o comportamento?
O BDD/Gherkin, pois é resumido, fácil de entender pela comunicação rápida e eficiente entre reuniões, pois já comunica como foi o comportamento do teste ou o que deveria ser, como não deveria, etc., com uma lógica já embutida para entender e quem lê já entenderá como.

### Qual seria mais fácil de manter?
O BDD/Ghenkir, por mais que o Tradicional seja bom para rescrever os passos ou demonstrar algo muito mais complicado de reproduzir.

---

  <div align="center">
    31/08/2026
  </div>
