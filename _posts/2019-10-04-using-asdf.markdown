---
layout: post
title:  "Using asdf"
description: Using asdf
date:   2019-10-04 17:00:36 +0530
categories: version manager asdf
---
Asdf is a extensible version manager via plugin. Asdf evaluate manager many CLI to multiple languages. For example Java, Node, Go, Haskell and much more.

First of all, we will installing asdf, the follow steps were extract of official documentation:

```sh
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.7.4
echo -e '\n. $HOME/.asdf/asdf.sh' >> ~/.bashrc
echo -e '\n. $HOME/.asdf/completions/asdf.bash' >> ~/.bashrc
```
Now, we can install plugin for any language, for instance:
```sh
asdf plugin-add nodejs https://github.com/asdf-vm/asdf-nodejs.git
asdf install nodejs 12.11.1
```


and that's all folks!

To any doubt, problem or suggestion, just say.
