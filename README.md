# Alocaí - Sistema SaaS de Alocação de Membros

Alocaí é um sistema SaaS desenvolvido para organizar e gerenciar a alocação de membros em projetos da GTi Engenharia Jr., empresa júnior vinculada aos cursos de Engenharia de Computação e Engenharia de Telecomunicações da Universidade Federal do Ceará (UFC).

<div align="center">
  <img  src="alocai.png" style="height: 240px; width: auto;">
</div>

## Lógica de Alocação

O sistema realiza um cálculo de disponibilidade que considera os cargos ocupados pelos membros e os projetos em que já estão envolvidos. A partir de uma pontuação gerada por esses fatores, é criado um ranking que identifica os membros com maior disponibilidade (ou seja, aqueles com menor pontuação). Dessa forma, evitamos a sobrecarga de determinados membros e garantimos uma distribuição mais equilibrada dos projetos, alinhando-se à meta de participação de todos.

## Peso do Cargo

Cada cargo na empresa possui um peso que reflete a carga de trabalho exigida na área de gestão. Por exemplo, um gerente comercial, com uma rotina mais intensa, tende a ter menos disponibilidade para assumir projetos simultâneos em comparação a um desenvolvedor, cuja principal função é a execução dos projetos.  
É importante notar que um cargo com alto peso não impede seu titular de participar de projetos; o ideal é que essa pessoa participe de, no mínimo, um projeto por ano, evitando atuar em mais de um projeto simultaneamente para não comprometer suas funções de gestão.

> **Peso Total do Cargo:**  
> É a soma dos pesos de todos os cargos que o membro ocupa.

## Peso do Projeto

Ao alocar um projeto para um membro, o sistema atribui um peso ao projeto, considerando seu tipo, complexidade e estado atual. Esse peso ajuda a mensurar a carga que o projeto representa, evitando que um membro já sobrecarregado com um projeto complexo assuma outro desafio semelhante, o que poderia comprometer a qualidade e a saúde do profissional.

O cálculo do peso de um projeto é feito da seguinte forma:

**Peso do Projeto = Fator do Tipo do Projeto × Fator de Complexidade × Fator do Estado do Projeto**

### Fator do Tipo do Projeto

- **Site:** 1  
- **Woocommerce:** 2  
- **Assessoria:** 2  
- **Sistema:** 4  

### Fator de Complexidade

- **Simples:** 1  
- **Intermediário:** 2  
- **Complexo:** 3  

### Fator do Estado do Projeto

(Varia entre 0 e 1)
- **Parado:** 0.2  
- **Início:** 1  
- **Middle:** 1  
- **Finalizando:** 1  
- **Suporte:** 0.5  

> **Peso Total dos Projetos:**  
> É a soma dos pesos de todos os projetos nos quais o membro está alocado.

## Cálculo de Disponibilidade

A pontuação final de um membro é a soma do peso total dos projetos e do peso total dos cargos que ele ocupa. Na aba de membros do sistema, os membros com menor pontuação são os que apresentam maior disponibilidade para novos projetos, permitindo uma alocação mais justa e eficiente.

---

Alocaí foi criado para facilitar a gestão dos projetos na GTi Engenharia Jr., garantindo uma distribuição equilibrada das tarefas e evitando a sobrecarga dos membros. Com uma abordagem inteligente e automatizada, nosso SaaS contribui para a maximização da eficiência e o sucesso dos projetos.
