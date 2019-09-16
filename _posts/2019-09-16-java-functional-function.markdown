---
layout: post
title:  "Conhecendo a Interface Function do Java"
description: Um exemplo simples usando a interface Functiona e Lambda
date:   2019-09-16 11:27:36 +0530
categories: Java8 Function Lambda
---
O Java 8 trouxe muitas novidades, uma delas foram as interfaces funcinais e o lambda.
É importante pensar em lambda como uma função, uma função anônima. Podemos usar um exemplo simples. Pense na seguinte expressão matemática:

```java
x = x + 1
```

Acima, temos o exemplo de uma função simples. Podemos expressar ela com o lambda e a interface java.util.Function:

```java
Function<Integer, Integer> myFunction = (x) -> x + 1;
```

Acima, estamos definindo uma função lambda. Para usar a mesma, basta:

```java
myFunction.apply(5)
```

E como resultado teríamos o valor 6.

Pronto, temos uma função.

Qualquer dúvida, problema ou sugestão é só dizer.

Segue o fonte: [Fontes](https://github.com/fagnercandido/codes/blob/master/java/Funcoes.java)