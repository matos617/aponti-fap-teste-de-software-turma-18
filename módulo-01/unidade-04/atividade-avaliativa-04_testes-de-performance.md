# Testes de Performance 

<details>
<summary>Atividade Avaliativa</summary>
  
## Atividade Avaliativa:
Dado um relatório de teste de performance, analise-o responder às seguintes questões:
- O sistema pode ser considerado aprovado?
- Quais métricas indicam problemas de performance?
- Quais possíveis gargalos podem existir?
- Esse cenário se aproxima mais de Carga, Stress ou Capacidade?
- O que você recomendaria ao time técnico?
</details>

(Clínica PSI como base)

### O sistema pode ser considerado aprovado?

Não. Como o sistema não passou na maioria dos testes e possui falhas importantes, ele não pode ser considerado aprovado. Além disso, o uso apenas do **storage do navegador** representa uma limitação importante para um sistema de clínica.

### Quais métricas indicam problemas de performance?

* Bugs de front-end em diferentes monitores;
* Tempo de resposta das funcionalidades;
* Perca e não recuperação de dados;
* Quantidade de erros durante o uso.

### Quais possíveis gargalos podem existir?

* Uso do **storage do navegador** para armazenar os dados;
* Limitação de espaço do armazenamento local;
* Risco de perda dos dados ao limpar o navegador ou trocar de dispositivo.

### Esse cenário se aproxima mais de Carga, Stress ou Capacidade?

Esse cenário se aproxima mais de um **teste de Capacidade**, pois o principal problema é verificar até que ponto o sistema consegue armazenar e manipular dados utilizando apenas o storage do navegador.

### O que você recomendaria ao time técnico?

Recomenda-se:

* Implementar um **banco de dados** adequado;
* Criar um servidor para armazenar e gerenciar os dados;
* Realizar testes de carga e capacidade;
* Corrigir as falhas funcionais identificadas;
* Melhorar a segurança e o controle de acesso;
* Realizar novos testes antes de considerar o sistema aprovado.

---

<div align="center">
 01/09/2026
</div>
