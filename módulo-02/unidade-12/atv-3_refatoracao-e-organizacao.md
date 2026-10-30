# Atividade 3: Refatoração e Organização
**Objetivo:** Explicar a importância de manter um código limpo, reutilizável e de fácil manutenção. 

**Enunciado:** Com base no módulo de "Refatoração e Organização", explique o que significa refatorar o código de um teste. Em sua resposta, você deve obrigatoriamente explicar o que é o princípio DRY (Don't Repeat Yourself) e detalhar pelo menos duas práticas de organização, como a criação de funções helper, o uso do beforeEach para preparar o estado antes de cada teste, ou a centralização de dados no arquivo constants.ts.

---

## O que significa refatorar o código de um teste?
Refatorar é melhorar a estrutura interna do código sem alterar o comportamento que ele verifica. O teste continua validando exatamente a mesma funcionalidade, mas fica mais legível, menos repetitivo e mais fácil de se manter.

## Princípio DRY (Don’t Repeat Yourself)
DRY significa “não se repita”: cada pedaço de conhecimento (um passo de login, uma URL, um seletor, um dado de teste) deve existir em um único lugar.

Se um mesmo trecho está copiado em vários testes, qualquer mudança na aplicação obriga em corrigir todos eles e esquecer um deixa um teste quebrado.

## Práticas de organização
### 1. Funções helper: Extraem passos repetidos para uma função reutilizável.

Sem o helper, você tem que escrever os mesmos passos em vários testes:
```typescript
await page.getByLabel('E-mail').fill('admin@teste.com');
await page.getByLabel('Senha').fill('123456');
await page.getByRole('button', { name: 'Entrar' }).click();
```

Com o helper, o teste fica mais limpo pois você importa do Helper. Se a tela de login mudar, só o helper precisa ser atualizado:
```typescript
// helpers/auth.ts
import { Page } from '@playwright/test';

export async function fazerLogin(page: Page, email: string, senha: string) {
  await page.getByLabel('E-mail').fill(email);
  await page.getByLabel('Senha').fill(senha);
  await page.getByRole('button', { name: 'Entrar' }).click();
}

// no teste:
await fazerLogin(page, 'admin@teste.com', '123456');
```

### 2. beforeEach para preparar o estado
`beforeEach` executa código antes de cada teste do grupo, sem repetir o setup dentro, para inicializar o ambiente sem afetar os outros testes que não utilizam essa função, tornando-as mais independentes entre si.
