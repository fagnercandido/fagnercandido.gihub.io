---
layout: post
title:  "Brazil Public Transparency"
description: Consuming API of Brazil Public Transparency
date:   2020-06-25 13:59:36 +0530
categories: python brazil public transparency
---

The Brazil Public Transparency has available one API to search all public data. You can search about anything relationship Governorment and costs.

The Swagger API it's available on: [Swagger API](http://www.portaltransparencia.gov.br/api-de-dados)

I made a little [script](https://github.com/fagnercandido/brazil-public-transparency/tree/master) that with an cnpj sum all values received and plot one bar graphic at the final process.

Some stranger things happended, for example, i was hoped one json and i received an html page,  :(, in this case, i was implemented one eternal retry to solve this.

Besides that, the API is not faster, so, in tests with one CPNJ in a period of 5 years, take some 30min to consumes all data.

and that's all folks!

If you have any doubts, problems or suggestions, just leave a message.
