---
layout: page
title: Instale o Ruby e o Ruby DevKit
nav_title: Ruby
step: 1
---

<a href="https://www.ruby-lang.org/pt/about/" target="_blank">Ruby</a> é a linguagem de programação na qual o <a href="http://jekyllrb.com" target="_blank">Jekyll</a> é desenvolvido. Você precisará instalar o Ruby e o <a href="http://rubyinstaller.org/add-ons/devkit/" target="_blank">DevKit</a> correspondente, que é necessário para compilar algumas das dependências do Jekyll como "extensões nativas".

## Instale o Ruby

Primeiro, clique no botão abaixo e baixe o instalador do Ruby 2.2.2 correspondente à arquitetura do seu sistema (x86 / x64).

<a href="http://rubyinstaller.org/downloads/" class="button-external" target="_blank">Baixe o Ruby para Windows</a>

Execute o instalador e avance pelas telas da instalação. Quando você chegar na tela abaixo, certifique-se de marcar a opção "*Add Ruby executables to your PATH*".

<img alt="Foto da última tela da instalação do Ruby" src="../public/img/ruby-path.png" class="img-nice">

Clique em "*Install*" e o Ruby será instalado em segundos.

## Instale o Ruby DevKit

O Jekyll tem algumas dependências que, a princípio, são fornecidas apenas na forma de código-fonte bruto. Para transformá-las em executáveis funcionais, você provavelmente precisará instalar o Ruby Development Kit.

Clique no botão abaixo e baixe o instalador do DevKit que corresponde à versão do Ruby que você instalou e à arquitetura do seu sistema. Para o Ruby 2.2.2, o nome do arquivo começará com `DevKit-mingw64`. Escolha a versão de 32 *bits* ou 64 *bits* dependendo do seu sistema.

<a href="http://rubyinstaller.org/downloads/" class="button-external" target="_blank">Baixe o Ruby DevKit</a>

O arquivo baixado é um arquivo auto-extraível. Quando você abri-lo, ele perguntará onde deve extrair os arquivos. Forneça um caminho que não contenha espaços. Recomendamos algo simples, como `C:\RubyDevKit\`. Clique em "*Extract*" e espere até que o processo termine.

Em seguida, você precisa inicializar o DevKit e associá-lo à sua instalação do Ruby. Abra a ferramenta de linha de comando de sua preferência e navegue até a pasta na qual você extraiu o DevKit.

~~~
cd C:\RubyDevKit
~~~

Auto-detecte as instalações do Ruby e as adicione a um arquivo de configuração para a próxima etapa.

~~~
ruby dk.rb init
~~~

Instale o DevKit, associando-o à sua instalação do Ruby.

~~~
ruby dk.rb install
~~~

## Resumo

Bom, é isso! Se tudo ocorreu bem, agora você possui uma instalação do Ruby funcionando na sua máquina e pode gerar executáveis funcionais usando o Ruby Development Kit. O Ruby inclui uma maneira de instalar as chamadas *gems* ("jóias") &mdash; pacotes de *software* que você pode usar a partir da linha de comando. O Jekyll é uma delas! Clique no botão abaixo para ver como você pode instalá-lo.

<div class="pagination">
  <a class="pagination-item older" href="{{ "/" | prepend: site.baseurl }}">&laquo; Introdução</a>
  <a class="pagination-item newer" href="{{ "/2-jekyll" | prepend: site.baseurl }}">Instalar o Jekyll &raquo;</a>
</div>
