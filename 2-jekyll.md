---
layout: page
title: Instale o Jekyll
step: 2
---

O próprio <a href="http://jekyllrb.com" target="_blank">Jekyll</a> é distribuído na forma de uma *gem* do <a href="https://www.ruby-lang.org/pt/about/" target="_blank">Ruby</a>, que é um pacote de *software* de fácil instalação. Para instalar o Jekyll e todas as suas dependências, abra a ferramenta de linha de comando de sua preferência e digite o comando a seguir.

~~~
gem install jekyll
~~~

Tecle Enter, assista e divirta-se. Isso pode demorar algum tempo, devido ao número de dependências.

## Compatibilidade

A versão mais recente do Jekyll até o momento em que este guia foi escrito é a 2.5.3, que é compatível com <a href="http://www.microsoft.com/pt-br/windows" target="_blank">Windows</a>. A maioria das versões anteriores também são. No entanto, não tente instalar o Jekyll 1.4.3, que é [incompatível com o Windows](https://github.com/jekyll/jekyll/issues/1948).

Volte aqui quando uma nova versão do Jekyll for lançada para saber se ela permanece compatível com o Windows.

## Resumo

Tcharam! Você instalou com sucesso o Jekyll. De fato, você já pode compilar e servir *sites* sem erros, a menos que eles possuam exemplos de código e você deseje usar realce de sintaxe para formatá-los. Para ver como configurar adequadamente um dos dois realçadores de sintaxe, clique no botão abaixo.

<div class="pagination">
  <a class="pagination-item older" href="{{ "/1-ruby-e-devkit" | prepend: site.baseurl }}">&laquo; Instalar o Ruby</a>
  <a class="pagination-item newer" href="{{ "/3-realce-de-sintaxe" | prepend: site.baseurl }}">Embelezar código &raquo;</a>
</div>
