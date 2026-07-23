# Testes Não-Funcionais

<details>
<summary>Atividade Avaliativa</summary>

Dado um sistema proposto, os alunos deverão elaborar um checklist de testes não funcionais, cobrindo obrigatoriamente:
- Performance
- Segurança
- Usabilidade
- Compatibilidade

Cada item do checklist deve indicar o que será verificado e qual o risco associado.
</details>

## Sistema Fictício - Plataforma de Agendamento de Consultas
A Plataforma (PACO) é um sistema web que permite que usuários realizem o agendamento de consultas médicas de forma simples e segura, enquanto administradores gerenciam horários e atendimentos.

| Integrações | Funcionalidades principais | Regras de negócio |
| --- | --- | --- |
| - Sistema acessado via navegador web | - Cadastro e autenticação de usuários | - Usuários devem estar autenticados para agendar consultas |
| - Usuários podem acessar por desktop, tablet ou celular | - Consulta de especialidades e profissionais disponíveis | - Não é permitido agendar dois horários simultâneos para o mesmo usuário |
| - Uso simultâneo por múltiplos usuários durante horários de pico | - Agendamento, cancelamento e visualização de consultas | - Cancelamentos só podem ocorrer até 24h antes da consulta |
|   | - Notificações de confirmação de agendamento | - Dados pessoais devem ser protegidos conforme boas práticas de segurança |
|   | - Área administrativa para gestão de horários |   |

### Checklist de Testes Não Funcionais – Plataforma PACO

#### 1. Performance

| ✔ | O que será verificado | Risco
| --- | --- | --- |
| ☐ | Tempo de resposta do login, pesquisa e agendamento (até 2 segundos) | Lentidão pode causar desistência dos usuários |
| ☐ | O funcionamento com múltiplos usuários acessando simultaneamente | Travamentos ou indisponibilidade em horários de pico
| ☐ | Consumo de CPU, memória e banco de dados durante alto uso | Sobrecarga dos servidores e queda de desempenho |
| ☐ | Estabilidade após uso contínuo (teste de duração) | Falhas, vazamento de memória ou reinicializações inesperadas
| - [] | | |

#### 2. Segurança
| ✔ | O que será verificado | Risco
| --- | --- | --- |
| ☐ | Apenas usuários autenticados conseguem agendar consultas | Acesso não autorizado ao sistema
| ☐ | Usuários comuns não acessam a área administrativa | Alteração indevida de horários e consultas
| ☐ | Dados pessoais são protegidos durante armazenamento e transmissão | Vazamento de informações dos pacientes
| ☐ | Sistema resiste a ataques como SQL Injection, XSS e força bruta | Invasão e comprometimento dos dados

#### 3. Usabilidade
| ✔ | O que será verificado | Risco
| --- | --- | --- |
| ☐ | Processo de cadastro e agendamento deve ser simples e intuitivo | Usuários cometem erros ou desistem da operação
| ☐ | Mensagens de erro e confirmação são claras e diretas | Confusão e utilização incorreta do sistema
| ☐ | Interface possui boa acessibilidade (contraste, teclado e leitores de tela) | Dificuldade de uso por pessoas com deficiência
| ☐ | Usuários conseguem aprender a utilizar o sistema sem treinamento | Aumento do tempo de aprendizado e suporte

#### 4. Compatibilidade

| ✔ | O que será verificado | Risco
| --- | --- | --- |
| ☐ | Funcionamento nos navegadores Chrome, Firefox, Edge e Safari | Recursos falham em alguns navegadores
| ☐ | Funcionamento em desktop, tablet e celular | Interface inadequada em determinados dispositivos
| ☐ | Layout responsivo em diferentes resoluções de tela | Má experiência de uso em telas pequenas ou grandes pela qualidade
| ☐ | Compatibilidade com Windows, Android, iOS e macOS | Usuários podem não conseguir acessar o sistema corretamente por não estar otimizado para outros sistemas

