<div align="center">
  
 # BDD

</div>


<details>

  <summary>Atividade Avaliativa</summary>

## Atividade Avaliativa
Escreva testes para uma funcionalidade de sua escolha no seu projeto
- Criar uma feature com descrição clara
- Criar 02 Cenários, contendo:
- Caminhinho feliz
- Caminhos alternativos usando “mas”
</details>

---

## Criar um perfil

### Funcionalidade: Criar Perfil
  **Como** administrador do sistema
  
  **Quero** criar novos perfis de usuário
  
  **Para** definir diferentes permissões de acesso ao sistema

<br>

### Cenário: Criar um novo perfil com sucesso
  **Dado** que o administrador está autenticado no sistema
  
  **E** acessou a funcionalidade "Perfis e Permissões"
  
  Quando cadastrar um novo perfil com dados válidos
  
  **E** definir as permissões do perfil
  
  **E** salvar o cadastro
  
  **Então** o perfil deve ser criado com sucesso
  
  **E** deve ser exibido na lista de perfis cadastrados
  
<br>

### Cenário: Tentar criar um perfil sem informações obrigatórias
  **Dado** que o administrador está autenticado no sistema
  
  **E** acessou a funcionalidade "Perfis e Permissões"
  
  **Quando** tentar cadastrar um novo perfil sem preencher os campos obrigatórios
  
  **Mas** tentar salvar o cadastro
  
  **Então** o sistema não deve criar o perfil
  
  **E** deve informar os campos obrigatórios que precisam ser preenchidos

  ---

  <div align="center">
    31/08/2026
  </div>
