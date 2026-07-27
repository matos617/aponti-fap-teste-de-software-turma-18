<div align="center">

# Parte 1 — Testes funcionais

</div>

<br>

##  Identificação das funcionalidades
| Funcionalidade | Objetivo | Usuário | Entrada principal | Resultado esperado | Possível erro |
| --- | --- | --- | --- | --- | --- |
| Cadastro de pacientes | Registrar novos pacientes no sistema | Recepcionista ou administrador | Nome, CPF, telefone, e-mail, endereço | Paciente cadastrado e disponível na base | CPF inválido, campos obrigatórios em branco, duplicidade de cadastro |
| Agendamento de consultas | Marcar consultas entre paciente e psicólogo | Recepcionista ou paciente | Nome do paciente, psicólogo, data e horário | Consulta registrada na agenda | Horário já ocupado, paciente inexistente, psicólogo indisponível |
| Reagendamento e cancelamento | Alterar ou cancelar consultas já marcadas | Recepcionista ou paciente | Consulta original, nova data/horário (se reagendar) | Consulta atualizada ou removida da agenda | Consulta não encontrada, novo horário indisponível |
| Registro de prontuários | Guardar informações clínicas e evolução do paciente | Psicólogo | Identificação do paciente, notas da sessão, evolução | Prontuário salvo e acessível para futuras consultas | Falha ao salvar, paciente não encontrado, acesso negado por perfil |
| Emissão de relatórios financeiros | Gerar relatórios de receitas e despesas da clínica | Administrador ou financeiro |  Período de análise, tipo de relatório | Relatório exibido ou exportado. | Período inválido, ausência de dados, falha na geração |

<br>

##  Testes Unitários
| Função/regra | Entrada | Resultado esperado | Por que é unitário? |
| --- | --- | --- | --- |
| Validação de CPF | “123.456.789-00” | Retorno “válido” ou “inválido” | Testa de forma isolada a regra de validação de CPF, sem depender de banco de dados ou interface e mostrando que o sistema rejeita CPFs incorretos |
| Validação do número do CRP | “12/34567” | Retorno “válido” ou “inválido” | Avalia apenas a regra de formatação e consistência do CRP |
| Cálculo do saldo financeiro | Receitas R$ 2.000; despesas R$ 800 | R$ 1.200 | Verifica isoladamente a fórmula de cálculo |
| Identificação de estoque abaixo do mínimo | Estoque atual = 3; mínimo = 5 | Alerta “estoque baixo” | Testa apenas a regra de comparação de valores |
| Validação de e-mail | “usuario@dominio.com” | Retorno “válido” ou “inválido” | Avalia isoladamente a regra de validação de formato de e-mail |

<br>

##  Testes de integração 
| Componentes integrados  | Ação | Resultado esperado | Risco |
| --- | --- | --- | --- |
| Cadastro de paciente com Banco de dados | Cadastrar novo paciente | Dados gravados corretamente no banco e paciente aparece na lista | Paciente não salvo ou duplicado |
| Agendamento + Agenda do psicólogo | Agendar consulta | Horário passa a constar como ocupado na agenda do psicólogo | Dois pacientes no mesmo horário |
| Check-in + Controle de presença | Realizar check-in do paciente na recepção | Presença registrada no sistema | Paciente não aparece como presente ou duplicidade de presença | 
| Consulta realizada + Lançamento financeiro | Finalizar consulta de paciente | Valor da sessão lançado automaticamente no financeiro | Consulta registrada sem cobrança ou cobrança duplicada |
| Compra de produto + Estoque | Registrar compra de produto | Quantidade adicionada ao estoque | Estoque não atualizado ou valor incorreto |

<br>

## 🖥️ Testes de sistema

### Cenário A — Atendimento completo
- **Pré-condições**: Sistema ativo; paciente não cadastrado.  
- **Dados utilizados**: Nome, CPF, telefone, psicólogo, data/hora da consulta, evolução da sessão, valor da consulta.  
- **Passos**:  
  1. Cadastrar paciente.  
  2. Localizar paciente.  
  3. Agendar consulta.  
  4. Fazer check-in.  
  5. Registrar evolução da sessão.  
  6. Lançar receita.  
  7. Conferir relatório financeiro.  
- **Resultado esperado**: Fluxo completo registrado sem falhas.  
- **Resultado obtido**: (preencher após execução).  
- **Situação**: Aprovado/Reprovado.  
- **Evidência**: Prints de cada etapa.  
- **Justificativa**: Teste de sistema porque cobre todo o ciclo de atendimento.  

### Cenário B — Reagendamento
- **Pré-condições**: Paciente e psicólogo cadastrados.  
- **Dados utilizados**: Consulta marcada para horário X.  
- **Passos**:  
  1. Criar agendamento.  
  2. Reagendar para novo horário.  
  3. Verificar liberação do horário anterior.  
  4. Conferir ocupação do novo horário.  
  5. Validar agenda atualizada.  
- **Resultado esperado**: Consulta movida corretamente, sem duplicidade.  
- **Resultado obtido**: (preencher após execução).  
- **Situação**: Aprovado/Reprovado.  
- **Evidência**: Prints da agenda antes e depois.  
- **Justificativa**: Teste de sistema porque envolve fluxo completo de reagendamento.  

### Cenário C — Controle de estoque
- **Pré-condições**: Produto não cadastrado.  
- **Dados utilizados**: Nome do produto, quantidade mínima, entradas e saídas.  
- **Passos**:  
  1. Cadastrar produto.  
  2. Registrar entrada.  
  3. Registrar saída.  
  4. Verificar quantidade final.  
  5. Conferir alerta de estoque mínimo.  
- **Resultado esperado**: Estoque atualizado corretamente e alerta exibido.  
- **Resultado obtido**: (preencher após execução).  
- **Situação**: Aprovado/Reprovado.  
- **Evidência**: Prints de cadastro, movimentação e alerta.  
- **Justificativa**: Teste de sistema porque cobre todo o ciclo de estoque.  

### Cenário D — Controle de acesso
- **Pré-condições**: Perfis criados (recepcionista e psicólogo).  
- **Dados utilizados**: Login e senha de cada perfil.  
- **Passos**:  
  1. Criar perfis com permissões diferentes.  
  2. Entrar como recepcionista.  
  3. Tentar acessar prontuários.  
  4. Entrar como psicólogo.  
  5. Validar acesso autorizado.  
- **Resultado esperado**: Recepcionista bloqueado; psicólogo autorizado.  
- **Resultado obtido**: (preencher após execução).  
- **Situação**: Aprovado/Reprovado.  
- **Evidência**: Prints das tentativas de acesso.  
- **Justificativa**: Teste de sistema porque avalia fluxo de login e permissões.

<br>

## Testes de aceitação

### 1. Agendamento sem conflito
- **Dado que** o paciente e o psicólogo estejam cadastrados,  
- **quando** a recepcionista tentar agendar uma consulta em um horário já ocupado,  
- **então** o sistema deverá impedir o agendamento e exibir uma mensagem de erro.  

### 2. Acesso a prontuários
- **Dado que** existam perfis diferentes no sistema,  
- **quando** um recepcionista tentar acessar os prontuários,  
- **então** o sistema deverá negar o acesso e exibir mensagem de permissão insuficiente.  

### 3. Atualização financeira
- **Dado que** uma receita ou despesa seja lançada,  
- **quando** o lançamento for confirmado,  
- **então** o sistema deverá atualizar automaticamente o saldo financeiro da clínica.  

### 4. Controle de estoque
- **Dado que** um produto esteja cadastrado com quantidade mínima definida,  
- **quando** o estoque atingir ou ficar abaixo desse valor,  
- **então** o sistema deverá emitir um alerta de estoque baixo.  

### 5. Localização de pacientes
- **Dado que** existam pacientes cadastrados,  
- **quando** o usuário pesquisar por nome ou CPF,  
- **então** o sistema deverá localizar e exibir o paciente correspondente.  


<br>

## 📝 Classificação dos testes

1. **Verificar se `receitas − despesas` retorna o saldo correto**  
   - **Classificação**: **Unitário**  
   - **Justificativa**: Testa isoladamente a regra de cálculo do saldo, sem depender de interface ou banco de dados.

2. **Verificar se uma receita salva aparece no relatório financeiro**  
   - **Classificação**: **Integração**  
   - **Justificativa**: Avalia se o módulo de lançamento de receita comunica corretamente com o módulo de relatórios.

3. **Executar todo o fluxo entre cadastro, atendimento e pagamento**  
   - **Classificação**: **Sistema**  
   - **Justificativa**: Testa o sistema completo, simulando o fluxo real de uso pelo usuário final.

4. **Confirmar com a direção da clínica se o relatório atende às necessidades administrativas**  
   - **Classificação**: **Aceitação**  
   - **Justificativa**: Verifica se o sistema atende às necessidades do negócio e pode ser aprovado pelo cliente.  

5. **Verificar isoladamente a validação de CPF**  
   - **Classificação**: **Unitário**  
   - **Justificativa**: Testa apenas a regra de validação de CPF, sem depender de outros componentes.  

6. **Verificar se um reagendamento atualiza a agenda**  
   - **Classificação**: **Integração**  
   - **Justificativa**: Avalia se o módulo de reagendamento comunica corretamente com a agenda do psicólogo.  

7. **Avaliar se apenas psicólogos podem visualizar prontuários**  
   - **Classificação**: **Sistema**  
   - **Justificativa**: Testa o controle de acesso dentro do sistema, simulando perfis diferentes.  

8. **Confirmar com a recepcionista se o processo de agendamento é adequado à rotina da clínica**  
   - **Classificação**: **Aceitação**  
   - **Justificativa**: Verifica se o sistema atende às necessidades práticas da recepcionista, sob o ponto de vista do usuário final.

<br>

---

# Parte 2 — Checklist de testes não funcionais

## 🔹 Performance

| O que verificar | Como verificar | Critério esperado | Risco | Prioridade |
|-----------------|----------------|-------------------|--------|------------|
| Tempo de carregamento da página inicial | Medir com cronômetro em diferentes dispositivos | Carregar em até 3 segundos | Lentidão no atendimento | Alta |
| Tempo para abrir a agenda | Testar com 100 agendamentos cadastrados | Abrir em até 2 segundos | Atraso no atendimento | Alta |
| Velocidade da pesquisa de pacientes | Pesquisar por nome e CPF em base com 1.000 registros | Resultado em até 2 segundos | Dificuldade em localizar pacientes | Alta |
| Tempo para salvar registros | Inserir dados de paciente e medir tempo de resposta | Salvar em até 1 segundo | Perda de produtividade | Média |
| Consumo de memória após uso prolongado | Usar o sistema por 2h e monitorar consumo | Não ultrapassar 500 MB | Travamento do navegador | Média |

## 🔹 Segurança

| O que verificar | Como verificar | Critério esperado | Risco | Prioridade |
|-----------------|----------------|-------------------|--------|------------|
| Acesso a prontuários sem autenticação | Tentar acessar URL diretamente sem login | Bloqueio imediato | Violação de sigilo | Alta |
| Restrição por perfil de usuário | Entrar como recepcionista e tentar acessar prontuários | Acesso negado | Exposição de dados sensíveis | Alta |
| Uso de senhas fracas | Tentar cadastrar senha "123456" | Bloqueio da senha | Invasão de contas | Alta |
| Expiração da sessão | Deixar sessão aberta por 30 min sem uso | Logout automático | Uso indevido por terceiros | Média |
| Entrada de scripts nos formulários | Inserir `<script>alert(1)</script>` em campo de texto | Bloqueio da entrada | Execução de código malicioso | Alta |

## 🔹 Usabilidade

| O que verificar | Como verificar | Critério esperado | Risco | Prioridade |
|-----------------|----------------|-------------------|--------|------------|
| Clareza dos nomes dos menus | Avaliar se os nomes são intuitivos | Menus claros e autoexplicativos | Dificuldade de uso | Média |
| Facilidade para cadastrar paciente | Contar número de etapas necessárias | Cadastro em até 3 etapas | Demora no atendimento | Alta |
| Mensagens de erro e sucesso | Inserir dados incorretos e observar mensagens | Mensagens claras e informativas | Cadastro incorreto | Média |
| Indicação de campos obrigatórios | Tentar salvar sem preencher campos obrigatórios | Sistema alerta o usuário | Dados incompletos | Alta |
| Navegação pelo teclado | Usar apenas TAB e ENTER para navegar | Navegação funcional | Barreiras para usuários com deficiência | Média |

## 🔹 Compatibilidade

| O que verificar | Como verificar | Critério esperado | Risco | Prioridade |
|-----------------|----------------|-------------------|--------|------------|
| Funcionamento em Chrome, Firefox e Edge | Abrir sistema em cada navegador | Funcionar sem falhas | Usuários sem acesso | Alta |
| Funcionamento em celular, tablet e computador | Testar em diferentes dispositivos | Layout responsivo | Tabelas cortadas em mobile | Alta |
| Diferentes resoluções (360px, 768px, 1366px) | Ajustar resolução da tela | Exibição correta | Layout quebrado | Média |
| Orientação vertical e horizontal | Rotacionar dispositivo móvel | Layout adaptado | Perda de dados visíveis | Média |
| Exibição correta de acentos e símbolos | Inserir nomes com acentos e caracteres especiais | Exibição correta | Dados ilegíveis | Média |

---

<div align="center">
  Domingo, dia 26 de Julho de 2026
</div>
