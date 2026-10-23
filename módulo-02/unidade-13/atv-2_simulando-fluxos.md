# Atividade 2: Simulando Fluxos com Ações
**Enunciado:** Para interagir com as páginas, o Playwright sincroniza automaticamente as ações.

**Sua Tarefa:** Escreva um pequeno trecho de código (em texto mesmo) simulando o preenchimento de um formulário de filtro de produtos, seguindo as boas práticas apresentadas na aula:
1. Preencha o campo de busca (id: #busca) com o texto "Notebook". (Lembre-se da recomendação sobre usar fill ao invés de type).
2. Selecione uma opção em um dropdown (menu suspenso) cujo localizador de automação é data-test="filtro-preco". A opção selecionada deve ter o value "menor-preco".
3. Clique no botão de buscar, utilizando a estratégia semântica getByRole para um botão com o nome "Buscar".
