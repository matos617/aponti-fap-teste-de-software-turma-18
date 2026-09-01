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

# 

```gherkin
Cenário: Cadastro de um novo perfil com sucesso

  Dado que o administrador está na funcionalidade de Perfis e Permissões
  Quando o administrador cadastra um novo perfil com informações válidas
  E define as permissões de acesso do perfil
  Então o sistema deve cadastrar o novo perfil com sucesso
  E o perfil deve ficar disponível para utilização no sistema
```
