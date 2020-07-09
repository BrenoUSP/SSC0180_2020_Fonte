# Fonte de Tensão
  Projeto de uma fonte de tensão ajustável de 3 a 12 Volts com capacidade de 100 mA, desenvolvido pelo aluno Breno Lívio Silva de Almeida (número USP 10276675).

## Objetivo
  Irá se partir da tensão da tomada (220V ou 127V) que vai ter que ser transformada de 127V/220V em Corrente Alternada (C.A.) em uma tensão adequada para alimentar nosso circuito. Isto é, de 3V-12V em Corrente Contínua (C.C.).

## Desenvolvimento do trabalho

### Componentes
|Nome|Quantidade|Especificações|Explicações|Preço Unitário|
|---|---|---|---|---|


### Cálculos

  Foi necessário realizar contas específicas se utilizando dos princípios da eletrônica para se obter os valores usados pelos componentes para se ter um circuito funcional. Primeiro deve-se calcular a tensão de pico primário, considerando a tensão de entrada sendo a fonte de alimentação de 127 V:

  <div align="center">
<p float="left">
  <img src="/images/eq1.png" width="150" />
</p>
</div>

  Em seguida calcula-se a tensão de pico secundário, levando-se o conta o ripple, na eletrônica é um valor residual e periódico obtido de uma fonte de tensão que, por sua vez, é alimentada por uma corrente alternada. Para isso busca-se um ripple de 10% da tensão de saída esperada de 25 V, ou seja, 2,5 V. Além disso, considera-se a tensão de um diodo de silício, em 0,65 V:

  <div align="center">
<p float="left">
  <img src="/images/eq2.png" width="300" />
</p>
</div>

  O período é dado por:

  <div align="center">
<p float="left">
  <img src="/images/eq3.png" width="50" />
</p>
</div>

  Com o período, encontra-se o tempo de carga:
  
  <div align="center">
<p float="left">
  <img src="/images/eq4.png" width="300" />
</p>
</div>

  Por fim, é possível encontrar a fórmula da capacitância, o que auxiliou a escolher um valor adequado para o componente de 330 µF, por ser acima do encontrado e por ser um valor comercial:
  
  <div align="center">
<p float="left">
  <img src="/images/eq5.png" width="200" />
</p>
</div>

### Simulador Falstad

<div align="center">
<p float="left">
  <img src="/images/falstad.png" width="900" />
</p>
</div>

[Link da simulação](http://tinyurl.com/y7hmerds)




Trabalho proposto pelo professor Eduardo Simões para a matéria de Eletrônica do Curso de Bacharelado em Ciências de Computação do Instituto de Ciências Matemáticas e de Computação (ICMC-USP).
