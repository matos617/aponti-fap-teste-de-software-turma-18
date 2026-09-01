  <div align="center">
    
  # Gherkin
  </div>

<details>

  <summary>Atividade Avaliativa</summary>

## Atividade Avaliativa
Escreva testes para uma funcionalidade de sua escolha no seu projeto
- Criar uma feature com descrição clara
- Criar 02 Cenários, contendo:
- Caminhinho feliz
- Caminhos alternativos usando “mas”

Checklist mental ao escrever Gherkin
- Está na terceira pessoa?
- Um comportamento por cenário?
- Ordem lógica respeitada?
- Linguagem de negócio?
- Leitura clara e natural?
</details>

---

## Funcionalidade: Criar perfil de usuário

  **Como** administrador do sistema
  **Quero** cadastrar novos perfis de usuário
  **Para** definir diferentes níveis de acesso e permissões no sistema

<br>

### Cenário: Cadastro de um novo perfil com sucesso
  **Dado** que o administrador está na funcionalidade de Perfis e Permissões
  **Quando** o administrador cadastra um novo perfil com informações válidas
  **E** define as permissões de acesso do perfil
  **Então** o sistema deve cadastrar o novo perfil com sucesso
  **E** o perfil deve ficar disponível para utilização no sistema

<br>

### Cenário: Tentativa de cadastro de perfil sem informações obrigatórias
  **Dado** que o administrador está na funcionalidade de Perfis e Permissões
  **Quando** o administrador tenta cadastrar um novo perfil sem preencher as informações obrigatórias
  **Mas** solicita o salvamento do cadastro
  **Então** o sistema não deve cadastrar o perfil
  **E** deve informar que existem informações obrigatórias não preenchidas

---

  <div align="center">
    31/08/2026
  </div>
