---
layout: page
title: Instale um realçador de sintaxe
step: 3
---

Seja utilizando Markdown ou HTML, o <a href="http://jekyllrb.com" target="_blank">Jekyll</a> facilita a exibição de códigos bonitos e legíveis nas páginas do seu *site*.

Por padrão, o Jekyll vem com o <a href="https://github.com/tmm1/pygments.rb" target="_blank">pygments.rb</a>, que é um realçador de sintaxe baseado no <a href="https://www.python.org/about/" target="_blank">Python</a>. Para utilizá-lo no <a href="http://www.microsoft.com/pt-br/windows" target="_blank">Windows</a>, você precisará instalar o Python e algumas ferramentas extras.

Uma boa alternativa é o <a href="http://rouge.jneen.net/" target="_blank">Rouge</a>, baseado no <a href="https://www.ruby-lang.org/pt/about/" target="_blank">Ruby</a>, que é mais rápido e mais fácil de instalar, mas não suporta tantas linguagens quanto o <a href="http://pygments.org/" target="_blank">Pygments</a>.

Abaixo, você encontratá instruções para ambos realçadores de sintaxe. Escolha o que melhor atende às suas necessidades. Mais informações podem ser obtidas no [*site* oficial do Jekyll](http://jekyllrb.com/docs/templates/#code-snippet-highlighting).

## Instale o Rouge

Rápido e sem complicação: abra a ferramenta de linha de comando de sua preferência e execute o comando a seguir.

~~~
gem install rouge
~~~

Em seguida, no arquivo `_config.yml` do seu *site*, defina o Rouge como seu realçador de sintaxe:

~~~
highlighter: rouge
~~~

Pronto!

## Faça o Pygments funcionar

Se quiser usar o Pygments, que é uma dependência do Jekyll por padrão, para realçar sintaxe no Windows, você precisará instalar o Python, o <a href="https://pip.pypa.io/" target="_blank">pip</a> e, finalmente, a base em Python para o pygments.rb.

**Observação:** uma vez que você termine de executar as etapas a seguir, o Jekyll pode ainda exibir erros enquanto compila ou serve *sites*. No entanto, esses erros não devem representar problemas de verdade, de modo que você pode ignorá-los com segurança.

### Instale o Python

A versão mais recente e que funciona do Python até o momento da escrita deste guia é a versão 2.7.10. O Python 3 não deve funcionar.<!-- TODO Verificar -->

Clique no botão abaixo e faça o *download* do instalador da versão 2.7.10 que corresponde à arquitetura do seu sistema (32 *bits* ou 64 *bits*).

<a href="http://www.python.org/download/" class="button-external" target="_blank">Baixe o Python</a>

Abra o arquivo baixado e avance pelas telas da instalação. Quando você chegar na tela abaixo, certifique-se de clicar na seta próxima à opção "*Add python.exe to Path*" e selecionar "*Entire feature will be installed on local hard drive*".

<img alt="Foto de tela da instalação do Python" src="../public/img/python-path.png" class="img-nice">

### Instale o pip

O pip é uma ferramenta para instalar e gerenciar pacotes do Python, similar às *gems* do Ruby. Você precisará dele para instalar o Pygments, o pacote do Python que o pygments.rb usa para formatar seu código.

O Python é instalado com o pip por padrão desde a versão 2.7.9, na série 2.x, ou desde a versão 3.4, na série 3.x. Se você utilizou o instalador do Windows para instalar o Python, o pip já deve estar instalado na sua máquina em `C:/Python27/Script` e essa pasta deve ter sido adicionada à sua variável de ambiente `PATH`. Senão, veja a seguir como instalar o pip manualmente.

Primeiro, clique no botão abaixo e baixe o arquivo `get-pip.py` usando o *link* disponibilizado no *site*.

<a href="https://pip.pypa.io/en/latest/installing.html" class="button-external" target="_blank">Baixe o pip</a>

Em seguida, abra a ferramenta de linha de comando de sua preferência e navegue até o local onde você baixou o arquivo `get-pip.py` (por exemplo, `C:\pip\` ou qualquer outro lugar onde você o baixou).

~~~
cd C:\pip
~~~

Então, execute o comando a seguir para automagicamente baixar e instalar todos os componentes necessários.

~~~
python get-pip.py
~~~

### Instale a base em Python do Pygments

Na linha de comando, execute o comando a seguir para instalar a base em Python do Pygments.

~~~
python -m pip install Pygments
~~~

### Defina o Pygments como seu realçador de sintaxe

Se ainda não fez isso, adicione a linha a seguir ao arquivo `_config.yml` do seu *site* para definir o Pygments como seu realçador de sintaxe.

~~~
highlighter: pygments
~~~

## Resumo

O Jekyll agora utilizará o realçador de sintaxe que você escolheu para fazer com que os códigos apresentados no seu *site* apareçam super bem. Estamos quase terminando. Clique no botão abaixo para ver como você pode fazer a opção super útil do Jekyll `--watch` funcionar no Windows. Ou, se você não pretende utilizá-la, [pule para algumas últimas dicas para rodar bem o Jekyll no Windows]({{ "/5-executando-o-jekyll" | prepend: site.baseurl }}).

<div class="pagination">
  <a class="pagination-item older" href="{{ "/2-jekyll" | prepend: site.baseurl }}">&laquo; Instalar o Jekyll</a>
  <a class="pagination-item newer" href="{{ "/4-wdm" | prepend: site.baseurl }}">Watch &raquo;</a>
</div>
