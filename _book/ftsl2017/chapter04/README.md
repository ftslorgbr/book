# Capítulo 4

# O Projeto Debian quer você!

## Debian

O Debian é uma organização formada por pessoas de todo o mundo dedicada ao desenvolvimento de Software Livre e a promoção dos ideais da comunidade de Software Livre. O Projeto Debian começou em 1993 com o objetivo de desenvolver um sistema operacional livre para computadores.  Traduzido para mais de 30 línguas, e suportando uma enorme variedade de arquiteturas de computadores, o Debian se intitula o sistema operacional universal e é hoje o maior projeto de Software Livre no mundo. Atualmente existem mais de 1.000 desenvolvedores oficiais do Debian e milhares de usuários que contribuem de alguma forma para o projeto.

Site do Projeto Debian: <http://debian.org>

## IX Fórum de Tecnologia em Software Livre - FTSL

O Fórum de Tecnologia em Software Livre - FTSL, é um evento anual, realizado em Curitiba - PR, sendo considerado o maior evento gratuito de Software Livre do Brasil, e tem como propósito a disseminação de novas tecnologias baseadas em Software Livre, bem como, a troca de experiências com as comunidades, universidades e empresas públicas e privadas, por meio de palestras, painéis e oficinas.

A 9a edição do FTSL aconteceu de 27 a 29 de setembro de 2017 no Campus central da Universidade Tecnológica Federal do Paraná - UTFPR.
No último dia do evento a comunidade Debian promoveu seis palestras na trilha chamada de minievento Debian. Minha palestra com o título **O Projeto Debian quer você!** foi a quarta realizada dentro deste minievento.

Site do FTSL: <http://debian.org>

Site da UTFPR: <http://utfpr.edu.br>

## O Projeto Debian quer você!

Nesta palestra considero que você já sabe o que é o Debian e que agora quer saber como contribuir para o Projeto. Portanto, não explico o que é uma distribuição, qual o origem do Debian, como o nome foi criado, o Debian Social Contract, quais os nomes das versões, quais as diferenças entre stable, testing e unstable e entre main, contrib e non-free, etc.

Para ver arquivos de apresentações realizadas pela comunidade Debian, incluindo algumas de introdução com abordagens mais básicas, acesse: <http://debianbrasil.org.br/apresentacoes>

Qualquer pessoa pode contribuir para o Projeto Debian, independente do seu nível de conhecimento. Você pode contribuir de forma anônima, ou se registrando na página Contributors para manter suas contribuições registradas. Para se registrar, acesse: <https://contributors.debian.org>

Depois que você se torna um contribuidor registrado, você pode participar dos processos para se tornar um membro oficial. Existem três tipos de contribuidores oficiais.

* DM - Debian Maintainer (Mantenedor Debian).
* DD - Debian Developer non-uploading (Desenvolvedor Debian sem permissão de upload).
* DD - Debian Developer uploading (Desenvolvedor Debian com permissão de upload).

Para obter mais informações sobre como se tornar um DM e um DD, acesse respectivamente: <https://wiki.debian.org/DebianMaintainer> e <https://wiki.debian.org/DebianDeveloper>

Você também pode assistir a palestra do João Eriberto Mota Filho sobre este tema realizada no FTSL no link <http://videos.softwarelivre.org/ftsl-2017/como-se-tornar-um-membro-oficial-do-debian-dd-ou-dm.html> e obter o arquivo da apresentação no link <http://www.eriberto.pro.br/palestras/debian-dd.pdf>

Vamos agora ver as formas para contribuir com o Projeto Debian.

### 0 - Empacotamento de software

O empacotamento de software é a principal forma de contribuir para o Debian, mas exige conhecimento técnico principalmente para usar o terminal. Contribuir com empacotamento permite que você se torne um DD uploading.

O empacotamento não foi abordado nesta palestra porque está disponível no YouTube uma série de vídeos tutoriais gravados João Eriberto Mota Filho com mais de 14 horas mostrando em detalhes como fazer empacotamento. Acesse o site do João Eriberto para ver mais detalhes: <http://debianet.com.br>

### 1 - Instale e use o Debian

A forma primária para contribuir para o Debian é: instalar e usar o Debian no seu computador ou notebook. Você pode obter uma cópia da imagem oficial do Debian neste link <https://www.debian.org/CD>. Basta você fazer o download, gravar em um DVD ou pendrive e instalar no seu equipamento.

Acesse este link para ver um site mais amigável para fazer o download: <http://get.debian.net>

A principal cópia do repositório do Debian no Brasil, chamado de espelho oficial, fica no Departamento de Informática da Universidade Federal do Paraná (DInf UFPR) e pode ser acesso neste link: <http://ftp.br.debian.org>

Ao instalar e usar o Debian, você:

* Terá testado o instalador.
* Aumentará a base de usuários.
* Ficará familiarizado com um sistema GNU/Linux.
* Ajudará na divulgação.

### 2 - Report bugs

Ao encontrar um problema no Debian, envie um bug report (relatório de erros) para que os Desenvolvedores fiquem sabendo e possam corrigi-lo. Acesse este link para saber como relatar um bug no Debian: <https://www.debian.org/Bugs/Reporting>

Você pode preencher o relatório via terminal com a ferramenta reportbug ou via interface gráfica usando a ferramenta reportbug-ng.

Os bugs no Debian possuem níveis de severidade:

* critical
* grave
* serious
* important
* normal
* minor
* wishlist

Alguns deste bugs são release-critical. Veja mais detalhes neste link: <https://bugs.debian.org/release-critical>

o DD Raphael Hertzog escreveu 7 dicas para enviar relatórios de bugs do Debian úteis e ter o seu problema resolvido (em inglês): <https://raphaelhertzog.com/go/bugreporting>

O Debian possui um Sistema de Acompanhamento de Bugs (BTS - Bug Tracking System) por meio do qual enviamos detalhes de bugs reportados por usuários e desenvolvedores. Cada bug é associado a um número e é mantido no arquivo até que seja marcado como tendo sido trabalhado. Mais detalhes neste link: <https://www.debian.org/Bugs>

Exemplos de bugs abertos no Gimp: <https://bugs.debian.org/cgi-bin/pkgreport.cgi?dist=unstable;package=gimp>

### 3 - Patches

Se você sabe como resolver um bug, você pode enviar um patch. Os Desenvolvedores irão analisar e se tudo estiver correto, eles aplicarão o seu patch dando o crédito a você pela ajuda, e assim você terá contribuído para o Debian.

### 4 - Documentação

Você pode produzir documentação para o Debian escrevendo:

* Manuais.
* Tutoriais.
* HOWTOs.
* FAQs.

Veja mais em <https://www.debian.org/doc> e <https://wiki.debian.org/Brasil/Documentos>

Você pode publicar tutoriais ensinando  a fazer alguma coisa no Debian, levando em consideração as seguintes ideias:

* Tema técnico ou não técnico.
* Nível básico ou avançado.
* Publicação escrita ou em vídeo.

Alguns sites de brasileiros com dicas e tutoriais:

* <http://eriberto.pro.br/blog>
* <http://blog.silva.eti.br>
* <http://softwarelivre.org/terceiro>
* <http://www.debiandicas.org>
* <http://www.debiandicas.com.br>
* <http://debianmaniaco.blogspot.com.br>

### 5 - Suporte a outros usuários

Outra forma importante de contribuir para o Debian é ajudando a tirar dúvidas de outros usuários. Existem muitos locais que você pode participar. Os meios oficiais do Projeto Debian são:

* Lista de discussão debian-user-portuguese:
    * <https://lists.debian.org/debian-user-portuguese>
    
* Canal no IRC:
    * Server: irc.debian.org
    * Canal: #debian-br

Nos últimos anos surgiram outros espaços não oficiais mantidos pela comunidade:

* Fórum
    * <http://www.forumdebian.com.br>

* Grupos no facebook:
    * <https://www.facebook.com/groups/DebianBR>
    * <https://www.facebook.com/groups/5366446847>

* Grupos no telegram:
    * <https://t.me/debianbrasil>

### 6 - Divulgação

Ajude a divulgar o Debian em espaços públicos onde tem pessoas com potencial para se tornarem usuárias do sistema operacional, como por exemplo:

* Sindicatos.
* Escolas.
* Universidades/Faculdades.
* Eventos como congressos, fóruns, encontros, etc.

Utilize seus perfis em redes sociais livres e fechadas para falar sobre Debian, encaminhar publicações de outras pessoas, divulgar os eventos e notícias relacionadas:

* Redes fechadas:
    * Twitter/Facebook/Google+

* Redes livres:
    * GNU Social <https://quitter.se>
    * Pump.io <http://pump.io>
    * Diaspora <https://diaspora.softwarelivre.org>
    * Hubzilla <https://hub.vilarejo.pro.br>

Use produtos com a logomarca Debian. A Comunidade Curitiba Livre vende vários produtos no site <http://loja.curitibalivre.org.br> e o lucro obtido é usado para organizar eventos de Software Livre em Curitiba. Nessa loja on-line você achará:

* Camisetas.
* Canecas.
* Bottons, chaveiros, cordões de crachá, adesivos, etc.

### 7 - Publicidade

O Projeto Debian tem um time de publicidade (Publicity Team) que elabora textos de notícias e mantém alguns sites relacionados. Esse time é responsável por publicar:

* Debian Press Release <https://www.debian.org/News>
* Debian Project News <https://www.debian.org/News/weekly>
* Debian Bits, the Debian Blog <https://bits.debian.org>
* Debian Micronews <https://micronews.debian.org>

O time de publicidade também mantém os perfis oficiais do Debian em redes sociais livres que você pode seguir:

* Pump.io <https://identi.ca/debian>
* GNU Social <https://quitter.se/debian>

E como você pode contribuir com o time de publicidade? Você pode contribuir escrevendo notícias ou revisando os textos de outras pessoas, mas para isso é imprescindível saber inglês. Mais informações em: <https://wiki.debian.org/Teams/Publicity>

Você pode ajudar com notícias em português enviando textos para o nosso blog da comunidade brasileira de usuários e desenvolvedores Debian. Obviamente esse blog não é oficial do Projeto Debian. Acesse: <http://debianbrasil.org.br>

### 8 - Organização de eventos

Todos os anos as comunidades ao redor do mundo organizam nas suas cidades o Debian Day para celebrar o aniversário do Debian que acontece em 16 de agosto (ou no sábado mais próximo). Você pode inscrever a sua cidade para participar no site: <https://wiki.debian.org/DebianDay>

No dia 17 de junho de 2017 foi lançada a nova versão do Debian - versão 9 chamada de Stretch. Veja algumas cidades que organizaram festas de lançamento (release party), inclusive no Brasil: <https://wiki.debian.org/ReleasePartyStretch>

Esses eventos podem ser desde um encontro em um bar ou em uma pizzaria, até um evento com palestras e oficinas relacionadas ao Debian. O importante é promover o encontro da comunidade local para celebrar o Debian.

### 9 - Produção de material gráfico

Você pode produzir materiais gráficos e disponibilizá-los para que outras pessoas utilizem livremente. Por exemplo:

* Desenhos para camisetas.
* Ícones.
* Logos.
* Mascotes.
* Temas/wallpapers.

Envie seu material para o Collab Debian, site que serve de repositório para as contribuições gráficas: <http://collab.debian.net>

O tema de cada versão do Debian é escolhido por votação, e qualquer pessoa pode enviar propostas. O tema da versão 6 do Debian, chamada de Squeeze, foi feita pelo brasileiro Valéssio Brito. Ele também criou a logo do Debian Day e é o mantenedor do projeto Collab Debian.

Os temas das duas últimas versões do Debian (8 - Jessie e 9 - Stretch) foram criados por Juliette "Taka" Belin, estudante francesa de programação de computadores e multimídia. O nome do tema da Jessie é Lines e do Stretch é Soft Waves. Para ver o portifólio da Juliette acesse o seu site pessoal <http://jbelin.com> e a sua galeria no DeviantArt <https://takaju.deviantart.com/gallery>

### 10 - Tradução

Uma das maiores contribuições que você pode dar ao Debian é ajudar a traduzi-lo do inglês para o português do Brasil. Normalmente os DDs non-uploading brasileiros contribuem intensamente com as traduções. O time brasileiro de tradução (L10n) mantém uma wiki com várias orientações para que você possa aprender e passar a colaborar: <https://wiki.debian.org/Brasil/Traduzir>

Veja a seguir as áreas que você pode traduzir, com trechos retirados da wiki do time brasileiro de tradução.

**DDTP - Debian Description Translation Packages**

O DDTP - Debian Description Translation Project (em português Projeto de Tradução das Descrições de Pacotes Debian), é um projeto internacional cujo principal objetivo é traduzir as descrições dos pacotes do Debian, dessa forma os usuários que não leem inglês terão mais facilidade em descobrir quais pacotes são úteis a eles. O DDTP foi implementado pelo alemão Michael Bramer e fornece a infraestrutura necessária para apoiar o processo de tradução e revisão. Veja mais detalhes e informações na página sobre o DDTP: <https://www.debian.org/international/l10n/ddtp>

Durante anos a principal interface com o DDTP foi o e-mail, até que Martijn van Oosterhout desenvolveu o DDTSS - Debian Distributed Translation Server Satellite (em português Satélite do Servidor de Traduções Distribuídas Debian). O DDTSS é uma interface web que interage com o DDTP e seu banco de dados, fornecendo um ciclo de tradução e revisão para os diferentes times de tradutores.

A equipe brasileira foi o segunda a aderir ao DDTP e se mantém entre as mais ativas, graças ao trabalho de muitos voluntários. É muito fácil colaborar com o DDTP já que o processo de tradução e revisão é feito pela web e os textos a serem traduzidos/revisados são normalmente pequenos. Um curto espaço de tempo por dia pode ajudar muito a equipe.

A ferramenta oficial de tradução do DDTP para a equipe brasileira é o DDTSS. Acesse a página da nossa equipe em: <http://ddtp2.debian.net/ddtss/index.cgi/pt_BR>

Para mais informações, acesse: <https://wiki.debian.org/Brasil/Traduzir/DDTP>

**Debian Installer (D-I) e Guia de Instalação**

Composto por dois componentes principais: o próprio instalador e o guia de instalação, requer trabalho continuado e alinhamento das traduções entre os materiais. Atualmente está 100% traduzido.

Felizmente, nossos esforços de tradução estão bastante avançados e atualmente os pacotes apt, dpkg, dselect, aptitude e outros, todos parte do sistema básico Debian, estão traduzidos para o idioma português do Brasil.

Para mais informações, acesse: <https://wiki.debian.org/Brasil/Traduzir/DI>

**Modelos debconf**

O projeto consiste na tradução dos arquivos do tipo POT utilizados pelo debconf, o sistema de configuração de pacotes da distribuição Debian, durante a instalação de pacotes no sistema.

Para mais informações, acesse: <https://wiki.debian.org/Brasil/Traduzir/DebConf>

**Páginas man**

Este projeto visa a tradução de páginas de manual de pacotes específicos do Debian, tais como debconf, fakeroot, dpkg e kernel-package. Pois já existe na ldp-br um projeto de tradução de páginas de manual mais comuns. 

Para mais informações, acesse: <https://wiki.debian.org/Brasil/Traduzir/ManPages>

**Páginas web**

Através das páginas web todos podem obter informações a respeito do Projeto Debian e suas diversas iniciativas. Para que as mesmas estejam disponíveis no idioma português do Brasil, uma equipe de tradutores, coordenada através da lista de discussão debian-l10n-portuguese, utiliza um sistema de controle de versão (CVS) onde os arquivos fonte, em formato WebWML (WML), ficam armazenados. Os mesmos são utilizados para geração das páginas em formato HTML durante o processo de reconstrução automática do site, que ocorre periodicamente.

Para mais informações, acesse: <https://wiki.debian.org/Brasil/Traduzir/WebWML>

As traduções dos arquivos POT e das páginas web WML seguem um ritual de envio de mensagens para a lista de discussão dos tradutores com o campo de assunto contento as seguintes siglas:

* ITT - Intent To Translate (intenção de traduzir).
* RFR - Request For Review (requisição para revisão).
* LCFC - Last Chance For Comment (última chance para comentários).
* DONE (feito).

Para mais informações, acesse: <https://wiki.debian.org/Brasil/Traduzir/Pseudo-urls>

O status das traduções pode ser visto na seguinta página: <https://l10n.debian.org/coordination/brazilian/pt_BR.by_status.html>

Uma boa dica é ver a palestra do Adriano Rafael Gomes no FISL16:

* Vídeo: <http://ur1.ca/qw5f8>
* Arquivo da apresentação: <https://bolicho.arg.eti.br/pub/eventos/2015/fisl16>

## Mensagem final

Espero que após ler este documento e acessar os links indicados, você se sinta encorajado(a) a contribuir com o Projeto Debian.

A comunidade brasileira é uma grande usuária de Software Livre, mas precisamos passar de meros usuários(as) para contribuidores(as) de fato. Seja com código ou com qualquer outro tipo de contribuição, todos nós podemos e devemos ajudar os projetos de Software Livre.

Quando você começar a contribuir para o Debian, descobrirá que a comunidade é muito receptiva e calorosa com os(as) novatos(as). O Projeto mantém várias inciativas para promover a diversidade. Leia mais sobre isso na página a seguir: <https://www.debian.org/intro/diversity>

**Venha fazer parte dessa comunidade incrível que é o Projeto Debian!**

## Minibiografia do autor

Paulo Henrique de Lima Santana.

Debian Maintainer (DM).

Bacharel em Ciência da Computação pela UFPR - Universidade Federal do Paraná.

Trabalha com administração de redes e sistemas GNU/Linux em Curitiba.

Entusiasta de Software Livre, participa de diversos grupos de atuação como a Comunidade Curitiba Livre (<http://curitibalivre.org.br>), o Grupo Debian Curitiba, e a ASL.Org - Associação Software Livre.Org (<http://asl.org.br>).

Palestrou em edições do FISL - Fórum Internacional Software Livre (<http://fisl.org.br>), da Latinoware - Congresso Latino-americano de Software Livre e Tecnologias Abertas (<http://latinoware.org>) e da Campus Party Brasil (<http://brasil.campus-party.org>).

Coordenou a organização de eventos em Curitiba como algumas edições do FLISOL - Festival Latino-americano de Instalação de Software Livre (<http://flisol.curitibalivre.org.br>), do SFD - Software Freedom Day (<http://sfd.curitibalivre.org.br>), do Circuito Curitibano de Software Livre (<http://circuito.curitibalivre.org.br>), e da MiniDebConf Curitiba (<http://br2016.mini.debconf.org> e <http://br2017.mini.debconf.org>).

Co-coordenou a organização da grade de programação do Fórum Internacional de Software Livre em 2015 (FISL16) e em 2016 (FISL17).

Curador de Software Livre da Campus Party Brasil desde 2013.

### Contatos:

E-mail: <phls@softwarelivre.org>

Site pessoal: <http://phls.com.br>

Perfil no telegram: @phls00

Perfis em redes sociais livres:

* <http://quitter.se/phls>
* <http://identi.ca/phls00>
* <http://diaspora.softwarelivre.org/u/phls>
* <http://hub.vilarejo.pro.br/channel/phls>

Perfis em redes sociais fechadas:

* <http://twitter.com/phls00>
* <http://facebook.com/phls00>

## Referências bibliográficas

Site do Debian: <https://www.debian.org>

Wiki do Debian: <https://wiki.debian.org>

Site da Comunidade Debian Brasil: <http://debianbrasil.org.br>

Site do FTSL - Fórum de Tecnologia em Software Livre: <http://ftsl.org.br>