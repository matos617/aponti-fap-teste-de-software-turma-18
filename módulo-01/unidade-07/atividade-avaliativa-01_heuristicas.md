<div align="center">
  
  # Heurísticas de Testes
</div>

<details>

  <summary>Atividade Avaliativa</summary>

## Atividade Avaliativa
- Aplique heurísticas de testes no seu projeto apra identificar riscos
- Escolha duas heurísticas + Nielsen ou Testing Tours
- Aplique a uma funcionalidade

Liste:
- Falhas
- Riscos identificados
- Áreas que merecem mais atenção
- Justifique usas escolhas
</details>

---

# Aplicação de Heurísticas de Teste na Funcionalidade de Exclusão de Perfil/Usuário

## 1. Funcionalidade analisada

**Funcionalidade:** Excluir perfil/usuário

**Objetivo:** Verificar se usuários que possuem permissão para serem excluídos são efetivamente removidos do sistema e perdem o acesso por meio de suas credenciais.

A funcionalidade foi analisada a partir do comportamento observado durante o teste de exclusão de um perfil de usuário.

---

## 2. Heurísticas escolhidas

* **Heurística de Estados e Transições**
* **Heurística de Erros**
* **Heurística de Nielsen: Visibilidade do Status do Sistema**

Essas abordagens foram selecionadas por serem adequadas para analisar uma funcionalidade crítica, na qual uma ação de exclusão deve provocar uma alteração real no estado do usuário e comunicar corretamente o resultado ao administrador.

---

## 3. Aplicação das heurísticas

### 3.1 Heurística de Estados e Transições

A heurística de Estados e Transições permite analisar como o sistema se comporta quando uma entidade passa de um estado para outro.

Na funcionalidade analisada, o usuário deveria passar pelo seguinte fluxo:

**Usuário ativo → Exclusão confirmada → Usuário removido/inativo → Acesso bloqueado**

Durante o teste, foi observado que o perfil desaparece da lista disponível no painel **Perfis e Permissões**, indicando visualmente que a exclusão foi realizada.

Entretanto, após sair do modo administrador e tentar acessar o sistema utilizando as credenciais do usuário excluído, o login foi realizado normalmente.

#### Falha identificada

O sistema apresenta o perfil como excluído no painel administrativo, mas mantém o usuário ativo no sistema de autenticação.

#### Risco identificado

Existe uma inconsistência entre o estado apresentado na interface e o estado real do usuário no sistema.

Um usuário que deveria estar excluído pode continuar acessando funcionalidades e informações do sistema.

#### Áreas que merecem mais atenção

* Atualização do status do usuário após a exclusão;
* Integração entre Perfis e Permissões e o sistema de autenticação;
* Persistência da exclusão no banco de dados;
* Controle de acesso após a exclusão.

<br>

### 3.2 Heurística de Erros

A heurística de Erros auxilia na identificação de situações em que o sistema pode apresentar comportamentos incorretos ou inesperados.

A exclusão de um usuário representa uma operação crítica, pois deveria remover o registro ou impedir permanentemente o acesso daquele usuário ao sistema.

O teste realizado verificou o comportamento do sistema após a confirmação da exclusão.

#### Falha identificada

Mesmo após o administrador excluir e confirmar a exclusão do perfil, o usuário associado continua conseguindo realizar login normalmente.

#### Risco identificado

A falha pode permitir que usuários que deveriam ter sido removidos continuem acessando o sistema.

Os principais riscos são:

* Acesso indevido ao sistema;
* Falha no controle de permissões;
* Possível exposição de informações;
* Inconsistência dos registros administrativos;
* Administradores acreditarem que um acesso foi removido quando ele continua ativo.

#### Áreas que merecem mais atenção

* Processo responsável pela exclusão do usuário;
* Validação da exclusão no banco de dados;
* Credenciais associadas ao perfil excluído;
* Controle de sessões e autenticação;
* Regras de negócio relacionadas à exclusão de usuários.

<br>

### 3.3 Heurística de Nielsen: Visibilidade do Status do Sistema

A heurística de **Visibilidade do Status do Sistema** estabelece que o sistema deve informar ao usuário de forma clara e correta o resultado de suas ações.

Após a confirmação da exclusão, o sistema remove o perfil da lista exibida ao administrador. Dessa forma, o sistema transmite a informação de que a exclusão foi realizada com sucesso.

Porém, o comportamento real demonstra que o usuário continua ativo, pois ainda consegue acessar o sistema utilizando suas credenciais.

#### Falha identificada

O sistema apresenta visualmente a exclusão como concluída, mesmo que o usuário continue possuindo acesso ao sistema.

#### Risco identificado

O administrador recebe uma informação incorreta sobre o resultado da operação e pode acreditar que o usuário não possui mais acesso.

Isso pode gerar uma falsa sensação de segurança e permitir acessos indevidos.

#### Áreas que merecem mais atenção

* Mensagens de confirmação da exclusão;
* Validação do resultado da operação;
* Sincronização entre a interface e os dados do sistema;
* Comunicação entre o módulo administrativo e o sistema de autenticação.

---

## 4. Justificativa das escolhas

As heurísticas foram escolhidas porque a funcionalidade de exclusão envolve uma alteração crítica no estado de um usuário.

A **Heurística de Estados e Transições** foi utilizada para verificar se o usuário realmente passa do estado de ativo para excluído ou inativo.

A **Heurística de Erros** foi escolhida para analisar possíveis comportamentos incorretos após uma operação crítica, como a exclusão de um usuário.

A **Heurística de Nielsen, Visibilidade do Status do Sistema**, foi aplicada porque o sistema apresenta visualmente a exclusão como realizada, mesmo que o comportamento posterior demonstre que o usuário continua ativo.

---

## 5. Conclusão
O sistema remove o registro da interface administrativa, dando a entender que a exclusão foi concluída. Entretanto, o usuário associado ao perfil continua conseguindo acessar o sistema normalmente utilizando suas credenciais.

A principal falha identificada está na inconsistência entre a exclusão apresentada visualmente e o comportamento do sistema.

A área que merece maior atenção é a integração entre o módulo **Perfis e Permissões**, o processo de exclusão do cadastro e o sistema de **autenticação**, porque a exclusão não está sendo refletida corretamente em todas as partes da aplicação.

---

<div align="center">
  31/09/2026
</div>
