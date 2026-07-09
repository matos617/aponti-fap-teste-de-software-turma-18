# Manifesto Ágil de Testes e Tendências

<details>
  <summary>Atividade:</summary>
  
Criar um quadro comparativo contendo:
- Práticas tradicionais de [**QA**](#qa-quality-assurance-ou-garantia-de-qualidade)
- Práticas modernas (Agile Testing, Automação, Shift Left, DevSecTestOps)
- Finalizar com uma reflexão escrita: 
  > “Quais desafios atuais de QA mais impactam projetos reais?”

</details>

---
<div align="center">
  
  ## Práticas tradicionais de QA vs Práticas modernas
</div>

| Aspecto | Práticas Tradicionais de QA | Práticas Modernas |
|:--------|:---------------------------|:------------------|
| Documentação | Extensa documentação, com muito esforço de manutenção. | Documentação clara e leve, para a comunicação ágil e maior colaboração. |
| Definição de qualidade | Qualidade baseada na conformidade com requisitos e normas. | Qualidade com foco no valor entregue ao cliente e [**UX**](#ux), além da entrega dos requisitos. |
| Plano de qualidade | Documento formal que descreve o produto e define os atributos de qualidade em prioridade. | Mais dinâmico e colaborativo que é ajustado/adaptado continuamente conforme feedback e mudanças.
| Momento dos testes | Testes concentrados nas fases finais do desenvolvimento para validação. | Testes contínuos desde o início do ciclo ([**“Shift Left”**](#shift-left)). |
| Responsabilidade | Equipes de QA separadas, responsáveis apenas pela qualidade e sem fazer parte do grupo de desenvolvimento | Qualidade é responsabilidade compartilhada por todos, com comunicação frequente, transparente e colaboração. |
| Automação | Predominância nos testes manuais. | Uso forte de testes automatizados ([**Integração CI/CD**](#integra%C3%A7%C3%A3o-cicd)). |
| Processo | Modelo sequencial | Metodologias ágeis, [**DevOps**](#devops), integrado ao [**Agile/Scrum**](#agilescrum)). |
| Feedback | Nas fases finais ou após a entrega | Rápido e contínuo, fazendo parte do desenvolvimento |
| Entrega | Grandes entregas, mas em intervalos longos. | Entregas pequenas frequentes e incrementais |
| Gestão de riscos | Correção de problemas após a sua identificação nas fases finais | Gerenciamento contínuo de riscos |
| Segurança | Era de forma separada e também nas fases finais | Adicionada desde o início ([**DevSecOps/DevSecTestOps**](#devsecopsdevsectestops)). | 

## “Quais desafios atuais de QA mais impactam projetos reais?”
Para mim, o maior desafio está na definição do que é qualidade e de como alcança-la. O conceito de qualidade é algo muito abstrato a sua avaliação é um processo subjetivo. Ao querer aplicá-la nos requisitos de um software/produto, se torna *"dificil escrever requisitos de software completos e inequivocos e é impossível medir diretamente determinadas características da qualidade (por exemplo, a manutenibilidade)"* [¹]. Todos os testes e evolução da garantia de qualidade se basearam nisto. Outra é que as especificações de um software integram requisitos de várias classes de stakeholders/clientes, mas pode acabar não incluindo todos os stakeholders/clientes e estes não considerarem o software de qualidade, por mais que este software atenda aos requisitos pré-estabelecidos [²]. Por isso se torna importante o feedback e a adaptabilidade do sistema, pois o objetivo se fixou na satisfação e experiência do cliente, mas e se as preferências do usuário mudarem? Então o sentido de qualidade muda, mesmo que pouco. 
O maior desafio dos projetos é saber chegar a um consenso e conseguir trabalhar isso em equipe, junto a organização, documentação e transparência para a colaboração, pois também haverá divergências sobre a qualidade entre a equipe, já que todos são ativos na sua garantia.

---

## :open_book: Dicionário:
- #### QA (Quality Assurance ou Garantia de qualidade)
  Práticas para garantir a alta qualidade do produto/software. Faz parte do Gerenciamento da Qualidade de Software, junto com o controle de qualidade.
- #### UX:
  Refere-se a *Experiência do Usuário* no software.
- #### Shift Left:
  Estratégia de antecipar trabalhos e validações (testes, segurança, observabilidade e performance), que tradicionalmente ocorriam nas fases finais do ciclo, para o início do desenvolvimento.
- #### Integração CI/CD:
- #### DevOps
- #### Agile/Scrum
- #### DevSecOps/DevSecTestOps

---

## Referências
- [[¹] e [²] Engenharia De Software 10e, de Ian Sommerville, Gerenciamento da qualidade, pág. 666, seção 24.1 - Qualidade de Software.](https://archive.org/details/sommerville-engenharia-de-software-10e/page/666/mode/2up)
- [Shifting from Traditional QA to Next Gen QA - Key Challenges.](https://www.linkedin.com/pulse/shifting-from-traditional-qa-next-gen-key-vyasaraj-padakandla-ad3zc/)

---

<div align="center">
Quarta-feira, dia 8 de Julho de 2026
</div>
