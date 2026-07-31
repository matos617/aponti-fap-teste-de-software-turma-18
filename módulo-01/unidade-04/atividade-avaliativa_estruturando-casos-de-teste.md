# Estruturando Casos de Teste

<details>
  <summary>Atividade Avaliativa:</summary>
A partir de comportamentos esperados em uma tela de login, crie pelo menos 10 casos de testes completos, aplicando os conceitos e estruturas vistos em aula.
Além do caminho feliz, pense em cenários alternativos que um bom tester faria (fora da caixinha)
Lembre-se: Linguagem clara e objetiva, steps bem separados, resultado esperado observável e sem termos genéricos.
</details>

## 🧪 Casos de Teste para Tela de Login

### CT-01
#### Login com credenciais válidas
- **Pré-condição:** Usuário possui conta ativa.  
- **Passos:**  
  1. Abrir tela de login
  2. Inserir e-mail válido cadastrado 
  3. Inserir senha correta
  4. Clicar em "Entrar"
- **Resultado esperado:** Usuário é autenticado e redirecionado para a página inicial do sistema
<br>
### CT-02
#### Login com senha incorreta
- **Pré-condição:** Usuário possui conta ativa.  
- **Passos:**  
  1. Abrir tela de login
  2. Inserir e-mail válido cadastrado 
  3. Inserir senha incorreta
  4. Clicar em "Entrar"
- **Resultado esperado:** Mensagem clara “Senha incorreta” exibida, sem acesso concedido

### CT-03
#### Login com e-mail não cadastrado
- **Pré-condição:** Usuário não usar dados de conta ativa/existentes 
- **Passos:**  
  1. Abrir tela de login
  2. Inserir e-mail inexistente 
  3. Inserir qualquer senha
  4. Clicar em "Entrar"
- **Resultado esperado:** Mensagem “Usuário não encontrado” exibida

### CT-04
#### Campos obrigatórios não preenchidos
- **Pré-condição:** Nenhuma
- **Passos:**  
  1. Abrir tela de login  
  2. Deixar campo de e-mail vazio 
  3. Inserir uma senha válida
  4. Clicar em "Entrar" 
- **Resultado esperado:** Exibir mensagem “Campo e-mail obrigatório”

*(Repetir também com a senha vazia.)*

### CT-05
#### Formato inválido de e-mail
- **Pré-condição:** Sistema disponível
- **Passos:**  
  1. Abrir tela de login  
  2. Inserir texto sem formato de e-mail (ex: “usuario123”)  
  3. Inserir senha válida
  4. Clicar em "Entrar"
- **Resultado esperado:** Mensagem “Formato de e-mail inválido” exibida

### CT-06
#### Tentativas múltiplas de login com falha
- **Pré-condição:** Sistema disponível
- **Passos:**  
  1. Inserir e-mail válido.  
  2. Inserir senha incorreta 5 vezes consecutivas  
- **Resultado esperado:** Conta bloqueada temporariamente com a mensagem “Conta bloqueada por tentativas inválidas. Tente novamente em X minutos”

### CT-07
#### Login com senha visível (teste de usabilidade)
- **Pré-condição:** Usuário possui conta ativa.  
- **Passos:**  
  1. Abrir tela de login
  2. Inserir senha
  3. Clicar no ícone “mostrar senha”
- **Resultado esperado:** A senha digitada torna-se visível, sem alterar valor

### CT-08
#### Login com caracteres especiais na senha
- **Passos:**  
  1. Abrir tela de login
  2. Inserir e-mail válido
  3. Inserir senha contendo caracteres especiais (ex.: `P@ssw0rd!`)
  4. Clicar em "Entrar"
- **Resultado esperado:** Login realizado com sucesso, com sistema aceitando os caracteres especiais

### CT-09
#### Login com teclado virtual (acessibilidade)
- **Pré-condição:** Usuário possui conta ativa.  
- **Passos:**  
  1. Abrir tela de login
  2. Inserir e-mail válido usando teclado virtual
  3. Inserir senha usando teclado virtual
  4. Clicar em "Entrar"
- **Resultado esperado:** Login realizado normalmente, sem nenhuma falha

### CT-10
### Login após sessão expirada
- **Pré-condição:** Usuário possui conta ativa.  
- **Passos:**  
  1. Usuário loga com sucesso.  
  2. Deixar sessão expirar (tempo configurado).  
  3. Tentar acessar página restrita sem re-logar.  
- **Resultado esperado:** Sistema redireciona para tela de login com mensagem “Sessão expirada, faça login novamente”.
