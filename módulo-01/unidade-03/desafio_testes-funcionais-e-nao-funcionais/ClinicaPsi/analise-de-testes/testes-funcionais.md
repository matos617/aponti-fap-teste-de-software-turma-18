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


##  Testes de integração 
| Componentes integrados  | Ação | Resultado esperado | Risco |
| --- | --- | --- | --- |
| Cadastro de paciente com Banco de dados | Cadastrar novo paciente | Dados gravados corretamente no banco e paciente aparece na lista | Paciente não salvo ou duplicado |
| Agendamento + Agenda do psicólogo | Agendar consulta | Horário passa a constar como ocupado na agenda do psicólogo | Dois pacientes no mesmo horário |
| Check-in + Controle de presença | Realizar check-in do paciente na recepção | Presença registrada no sistema | Paciente não aparece como presente ou duplicidade de presença | 
| Consulta realizada + Lançamento financeiro | Finalizar consulta de paciente | Valor da sessão lançado automaticamente no financeiro | Consulta registrada sem cobrança ou cobrança duplicada |
| Compra de produto + Estoque | Registrar compra de produto | Quantidade adicionada ao estoque | Estoque não atualizado ou valor incorreto |

##  
| Função/regra | Entrada | Resultado esperado | Por que é unitário? |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

##  
| Função/regra | Entrada | Resultado esperado | Por que é unitário? |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

##  
| Função/regra | Entrada | Resultado esperado | Por que é unitário? |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |
