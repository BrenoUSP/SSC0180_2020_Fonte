# Fonte de Tensão
  Projeto de uma fonte de tensão ajustável de 3 a 12 Volts com capacidade de 100 mA, desenvolvido pelo aluno Breno Lívio Silva de Almeida (número USP 10276675).

## Objetivo
  Irá se partir da tensão da tomada (220V ou 127V) que vai ter que ser transformada de 127V/220V em Corrente Alternada (C.A.) em uma tensão adequada para alimentar nosso circuito. Isto é, de 3V-12V em Corrente Contínua (C.C.).

## Desenvolvimento do trabalho

### Componentes
|Nome|Quantidade|Especificações|Explicações|Preço Unitário|
|---|---|---|---|---|
| **Fonte de alimentação** |**1**| **Energia da tomada**| Fonte de energia 127V | ----------- | 
| **Interruptor** |**1**| **250 V e 3 A**| Apenas para ligar e desligar o circuito | [R$28,89](https://produto.mercadolivre.com.br/MLB-1300399738-boto-chave-gangorra-mini-interruptor-liga-desliga-on-off-10x15mm-kcd13-101-3a-250v-arduino-_JM) | 
|**Transformador**|**1**| **bivolt, 15 V e 500 mA**  | Esse transformador foi escolhido visando garantir  uma margem de erro confortável para quedas de tensão nos componentes, além de ser bivolt, podendo lidar com 127V/220V|[R$44,89](https://produto.mercadolivre.com.br/MLB-1305497792-transformador-1515v-2a-trafo-bivolt-_JM) |
|**Ponte Retificadora**|**1**| **1000 V e 2 A** | Responsável por fazer a conversão correta de C.A. para C.C. | [R$3,07](https://produto.mercadolivre.com.br/MLB-1151520283-ponte-retificadora-2w10-2a-1000v-lote-com-10-pecas-_JM)|
|**Capacitor**|**1**| **330 uf/35 V** | Usado para estabilização da tensão do circuito, armazenando energia. O valor se chegou demonstrado pelos cálculos que vão ser explicados em seguida |[R$2,62](https://produto.mercadolivre.com.br/MLB-1475685583-20x-capacitor-eletrolitico-330uf35v-smd-105-10x102mm-_JM)|
|**Diodo Zener**|**1**| **13 V - 0,5 W** | Regula a tensão a 13 V |[R$0,32](https://produto.mercadolivre.com.br/MLB-1395521239-diodo-zener-13v-05w-1n5243-lote-de-100-pecas-_JM)|
|**Transistor**|**1**| **2N2222A** | Atenua a corrente e a tensão. Corrente máxima no coletor de 0.8 mA e tensão máxima do coletor 75V  |[R$1,05](https://produto.mercadolivre.com.br/MLB-1222136291-20-pecas-transistor-npn-2n2222a-_JM) |
|**Resistência**|**2**| **5K6 ohms** | Utilizada para limitar a tensão no zener de modo que está fique na faixa de 13V  |[R$1,08](https://produto.mercadolivre.com.br/MLB-1388075980-50un-resistor-1w-de-potencia-escolha-1-valor-ohmico-na-lista-_JM) |
|**Potenciômetro**|**1**| **10k ohm**  | Mantém a tensão entre 0V e 12V | [R$2,8](https://produto.mercadolivre.com.br/MLB-882483201-10x-potencimetro-10k-linear-com-eixo-l20-estriado-_JM)|

|**Preço total**|
|---|
|R$84,72|

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
