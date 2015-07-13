---
layout: page
title: Use o jekyll --watch
step: 4
---

O <a href="http://jekyllrb.com" target="_blank">Jekyll</a> tem uma funcionalidade integrada de auto-regeneração que reconstrói o seu *site* quando observa mudanças no código-fonte. Desde a versão 2.4.0 do Jekyll, o comando `jekyll serve` tem essa funcionalidade habilitada por padrão e você pode utilizar `jekyll build --watch` para habilitá-la manualmente.

## Instale a *gem* wdm

No <a href="http://www.microsoft.com/pt-br/windows" target="_blank">Windows</a>, você precisa instalar uma ferramenta extra, ou *gem*, para habilitar essa funcionalidade. Simplesmente execute o comando a seguir na linha de comando.

~~~
gem install wdm
~~~

## Exija a wdm no seu Gemfile

Como alternativa, se você utiliza um `Gemfile`, pode verificar se o Jekyll está sendo executado no Windows e somente nessa ocasião instalar a *gem* <a href="https://github.com/Maher4Ever/wdm" target="_blank">wdm</a>.

~~~
gem 'wdm', '~> 0.1.0' if Gem.win_platform?
~~~

## Instale uma versão da *gem* listen que funcione

O Jekyll requer a *gem* <a href="https://github.com/guard/listen" target="_blank">listen</a> como dependência para a auto-regeneração. Algumas versões da listen não funcionam no Windows. [Essa página](https://github.com/jekyll/jekyll-help/issues/64) tem mais informações sobre versões que funcionaram no Windows no passado. Você pode verificar na [tabela de versões]({{ "/#versoes" | prepend: site.baseurl }}) quais versões da listen foram testadas durante a elaboração deste guia.

## Pode ainda não funcionar

- Se você tentar executar `jekyll build --watch` ou `jekyll serve` e o diretório de saída já existir, às vezes o Jekyll falha durante a compilação do *site*. Se você se deparar com esse problema, você pode contorná-lo adicionando `--force_polling` ao final do seu comando para o Jekyll. Veja as discussões [aqui](https://github.com/twbs/bootstrap/pull/14746) e [aqui](https://github.com/jekyll/jekyll/issues/2926) para mais informações.

- Às vezes, a auto-regeneração do Jekyll não funciona de forma alguma. [Essa página](https://github.com/jekyll/jekyll/issues/2529) sugere que ela não funciona em sistemas de 32 *bits* e não há solução conhecida. Desde a versão 2.4.0 do Jekyll, se seu sistema é afetado por esse problema, você precisa manualmente desabilitar a funcionalidade de auto-regeneração quando desejar que o Jekyll sirva seu *site* executando `jekyll serve --no-watch`.

## Resumo

Respire fundo! Você já instalou tudo que precisa para executar o Jekyll no Windows. Há ainda alguns detalhes aos quais você precisa se atentar para se certificar de que seus *sites* sejam compilados bem e sem complicações. Clique no botão abaixo para continuar.

<div class="pagination">
  <a class="pagination-item older" href="{{ "/3-realce-de-sintaxe" | prepend: site.baseurl }}">&laquo; Embelezar código</a>
  <a class="pagination-item newer" href="{{ "/5-executando-o-jekyll" | prepend: site.baseurl }}">Executar o Jekyll &raquo;</a>
</div>
