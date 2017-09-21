# FTSL Book

Este é um repositório para livros sobre software livre com conteúdo produzido pelos participantes do Fórum de Tecnologia em Software Livre de Curitiba.

Para cada do evento, iniciando em 2017, vamos produzir um livro, no qual os capítulos serão produzidos por palestrantes e instrutores.

O projeto está aberto para os contribuidores não somente enviem seus textos, mas possam ver em suas próprias máquinas como o livro todo até o ponto em que foi produzido.

# Como escrever os capítulos

**Procedimentos iniciais:**

* Abra uma [issue](https://github.com/ftslorgbr/book/issues);
* Como título da issue coloque o nome do capítulo que irá escrever: Capítulo N;
* Faça um commit inicial criando a pasta do capítulo com o arquivo README.md dentro;

Estes procedimentos irão "marcar território" - todos saberão que alguém vai escrever aquele capítulo e assim não criarão (intencionalmente) uma pasta igual.
A partir desse commit, pode fazer a escrita localmente e escolher se vai subindo as alterações aos poucos ou quando terminar tudo.

Se tiver dúvidas sobre GIT, o [Guia de Roger Dudler](http://rogerdudler.github.io/git-guide/index.pt_BR.html) é uma boa referência.

A construção dos capítulos deverá seguir as regras abaixo. É essencial lê-las.

# Regras para produção do livro

* Um livro (pelo menos) será produzido por ano, a partir de 2017;
* Cada livro estará em uma pasta com o nome ftsl[ano];
* A estrutura de cada livro segue este modelo :

```
SUMMARY.md 
chapter01
--README.md
chapter02
--images
--chapter02.01
...
--chapter02.mm
--README.md
...
chapterNN
--README.md
```
Onde cada capítulo está em uma pasta chapter[numero] que contém um arquivo README.md com o conteúdo do capítulo.

* O arquivo SUMMARY.md contém o índice do livro. Cada capítulo adicionado deve ser referido neste arquivo;
* Os arquivos README.md deverão conter no mínimo 2500 caracteres e no máximo 5000, excluindo imagens, mini-biografia e referências bibliográficas;
* As imagens usadas no capítulo deverão estar em uma pasta images dentro da pasta do capítulo;
* O nome dos arquivos de imagens deverá seguir o modelo chapterNN.mm onde NN é o numero do capítulo e mm é a sequência da imagem no capítulo;
* Todo capítulo deverá terminar com as referências bibliográficas das citações usadas no capítulo;
* Antes das referências bibliográficas deverá haver uma mini-biografia do autor, com no máximo 500 caracteres, em terceira pessoa;
* O capítulo deverá obrigatoriamente conter o título e o nome do autor;

Para gerar o livro localmente e vê-lo em seu navegador, você pode usar o Gitbook, seguindo as instruções abaixo.

# Configuração e Instalação do GitBook

### Instalação local

##### Requisitos

Instalar GitBook é fácil. Seu sistema apenas precisa atender a este dois requisitos:

* NodeJS (v4.0.0 e superior é recomendado)
* Windows, Linux, Unix, ou Mac OS X

##### Instale com NPM

O melhor modo de instalar GitBook é via **NPM**. No prompt do terminal, simplesmente rode o seguinte comando para instalar Gitbook:

```
$ npm install gitbook-cli -g
```

`gitbook-cli` é um utilitário para instalar e usar múltiplas verões de GitBook sobre o mesmo sistema. Ele automaticamente instalará a versão requerida de Gitbook para construir um livro.

##### Crie um livro

GitBook pode iniciar uma estrutura de livro:

```
$ gitbook init
```

Se você deseja criar o livro em um novo diretório, você pode fazer isso rodando `gitbook init ./directory`

Para visualizar e publicar seu livro use:

```
$ gitbook serve
```

Ou construa o website estático usando:

```
$ gitbook build
```

Os comandos anteriores devem ser executados dentro da pasta de cada livro. Não execute na raiz do projeto.


# Gerando eBooks e PDFs

GitBook pode gerar um website, mas também pode gerar conteúdo como ebook (ePub, Mobi, PDF).

## Gerando um arquivo PDF

```
$ gitbook pdf ./ ./mybook.pdf
```
## Gerando um arquivo ePub

```
$ gitbook epub ./ ./mybook.epub
```
## Gerando um arquivo Mobi

```
$ gitbook mobi ./ ./mybook.mobi
```

## Instalando ebook-convert

ebook-convert é requerido para gerar ebooks (epub, mobi, pdf).

### GNU/Linux

Instale e aplicação Calibre.

$ sudo aptitude install calibre

Em algumas distribuições GNU/Linux node é instalado como nodejs, então você precisa criar manualmente um link simbólico:

```
$sudo ln -s /usr/bin/nodejs /usr/bin/node
```

### OS X

Baixe a aplicação Calibre. Depois de mover calibre.app para sua pasta Applications crie um link simbólico para a ferramenta ebook-convert:

```
$ sudo ln -s ~/Applications/calibre.app/Contents/MacOS/ebook-convert /usr/bin
```

Você pode substituir /usr/bin com qualquer diretório que está em seu $PATH.


# A capa

A capa do livro é definida por um arquivo cover.jpg no diretório raiz do livro. Uma miniatura da capa é definida pelo arquivo cover_small.jpg. O arquivo da capa deve estar no formato JPEG. A capa é decidida por democracia em consenso com os que puderem contribuir com a produção gráfica, respeitando os seguintes requisitos:

* Tamanho de 1800x2360 para cover.jpg e 200x262 para cover_small.jpg;
* Sem borda;
* Título do livro claramente visível;
* Qualquer texto importante deve estar visível na miniatura.

