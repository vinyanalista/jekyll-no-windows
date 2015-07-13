---
layout: page
title: Execute o Jekyll sem erros
step: 5
---

## Caracteres `BOM` não são permitidos

Se houver quaisquer caracteres `BOM` no cabeçalho dos seus arquivos codificados como UTF-8, o <a href="http://jekyllrb.com" target="_blank">Jekyll</a> vai travar. Certifique-se de que não há.

## Altere a codificação dos seus arquivos para UTF-8

Dependendo da versão do <a href="https://www.ruby-lang.org/pt/about/" target="_blank">Ruby</a> e/ou do Jekyll que você usa, do conteúdo do seu *site*, e possivelmente de outros fatores, talvez você precise se certificar de que o Jekyll lerá o código-fonte do seu *site* como UTF-8.

Se você seguiu este guia passo-a-passo ou se suas versões correspondem às [versões usadas neste guia]({{ "/#versoes" | prepend: site.baseurl }}), provavelmente não é necessário realizar os reparos indicados a seguir.

### Defina a opção `encoding`

Desde a versão 1.3.0 do Jekyll, você pode definir a codificação do seu *site* no arquivo `_config.yml`:

~~~
encoding: utf-8
~~~

### Altere a codificação do console

Ao invés disso, você pode mudar a codificação da sua ferramenta de linha de comando para UTF-8 executando o comando a seguir toda vez em que abrir uma nova janela de console.

~~~
chcp 65001
~~~

## Use subdiretórios

O Jekyll não consegue compilar ou servir *sites* de certos diretórios reservados do <a href="http://www.microsoft.com/pt-br/windows" target="_blank">Windows</a>, como seu diretório de usuário. Ao invés disso, ele informará um erro parecido com este:

{% highlight text %}
C:\Users\SeuNome>jekyll serve
Configuration file: C:\Users\SeuNome\_config.yml
            Source: C:\Users\SeuNome
       Destination: C:\Users\SeuNome\_site
      Generating...
jekyll 2.5.3 | Error:  Permission denied @ dir_initialize - .
{% endhighlight %}

Se você encontrar um erro como esse, mova seu *site* para um subdiretório (por exemplo, `C:\Users\SeuNome\site-maneiro-com-jekyll`) e tente novamente.

## Fim

{% highlight text %}
jekyll build
jekyll build --watch
jekyll build -w
jekyll serve
jekyll serve --watch
jekyll serve -w
{% endhighlight %}

Agora você pode executar todos os comandos acima no seu computador com Windows. Parabéns: você instalou o Jekyll no Windows com sucesso!

Achou que algo não ficou muito claro? Algo neste guia está desatualizado? Esqueci alguma coisa? Por favor, verifique se alguém já percebeu na [lista de problemas conhecidos deste guia](https://github.com/vinyanalista/jekyll-no-windows/issues?state=open) ou [reporte um novo problema no GitHub](https://github.com/vinyanalista/jekyll-no-windows/issues/new) se não for o caso. Obrigado!

Se precisar de ajuda sobre como usar o Jekyll de uma maneira em geral, visite o *site* oficial do Jekyll clicando no botão abaixo.

<div class="pagination">
  <a class="pagination-item older" href="{{ "/4-wdm" | prepend: site.baseurl }}">&laquo; Watch</a>
  <a class="pagination-item newer" href="http://jekyllrb.com" target="_blank"><em>Site</em> do Jekyll &raquo;</a>
</div>
