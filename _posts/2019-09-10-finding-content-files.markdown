---
layout: post
title:  "Localizar texto dentro de arquivos .gz"
description: Um exemplo de como localizar textos dentro de arquivos .gz.
date:   2019-09-10 12:27:36 +0530
categories: Linux Linha de Comando
---
Recentemente precisei pesquisar em arquivos .gz. O detalhe é que haviam vários arquivos, e não sabia exatamente em qual encontrar.
Para tanto, basta realizar o seguinte:

```sh
find . -name "*.gz" -exec zgrep -H 'padraoASerProcurado' \{\} \;
```

Na linha de comando acima, ele irá pesquisar em todos os arquivos do diretório corrente, pelo padrão informado. Além disso, o argumento -H, informa o nome do arquivo.

