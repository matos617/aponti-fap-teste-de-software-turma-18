# Parte 1 — Testes funcionais

##  Identificação das funcionalidades
| Funcionalidade | Usuário | Entrada principal | Resultado esperado | Possível erro |
| --- | --- | --- | --- | --- |
| Cadastro de pacientes | Cadastro de pacientes | Nome, CPF, telefone, e-mail, endereço | Paciente cadastrado e disponível na base | CPF inválido, campos obrigatórios em branco, duplicidade de cadastro |
| Agendamento de consultas | Marcar consultas entre paciente e psicólogo | Recepcionista ou paciente (via sistema) | Nome do paciente, psicólogo, data e horário | Consulta registrada na agenda | Horário já ocupado, paciente inexistente, psicólogo indisponível |
