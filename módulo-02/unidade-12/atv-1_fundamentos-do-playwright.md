# Atividade 1: Fundamentos do Playwright (Envio de Texto)
**Objetivo:** Consolidar o entendimento teórico sobre o Playwright e o conceito de testes de fluxo completo. Enunciado: Responda com suas palavras:
1. O que é o Playwright e para que ele serve?
2. Qual é a principal diferença entre um teste E2E (End-to-End) e um teste unitário? Inclua na sua resposta como o teste E2E lida com a visão do usuário final e os cenários felizes e de erro.

---

## 1. O que é o Playwright e pra quê ele serve?

Playwright é uma ferramenta framework para testes E2E na web moderna. Construída pela Microsoft, ela permite controlar os principais navegadores usados: Chrome, Firefox, Edge e Safari (ou seja, multinavegadores), para similar a ação de um usuário nos testes automotizados.

## 2. Qual é a principal diferença entre um teste E2E e um teste unitário?

Enquanto o teste unitário foca em um teste de uma função/funcionalidade específica do código, o E2E simula toda a jornada que um usuário real faz no sistema, desde o login ou cadastro, movimentação no menu principal, compra ou envio, até sua saída do sistema. Então o E2E irá envolver mais de uma funcionalidade, também testando os caminhos felizes (que remetem a trajetória desejada e correta a passar), como também os testes de caminho infeliz ou de erro (que irá procurar por falhas e erros, ou até como o sistema age com o erro, que o usuário final encontraria no produto), assim, reduzindo custos de manutenções futuras.

---

Fontes:
- [Introdução ao Playwright para testes de ponta a ponta - Microsoft](https://learn.microsoft.com/pt-pt/shows/getting-started-with-end-to-end-testing-with-playwright/introduction-to-playwright-for-end-to-end-testing)
