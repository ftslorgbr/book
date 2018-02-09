# Capítulo 8 

**Computação Paralela com MPI (Message Passing Interface)**

_Sidney Batista Filho_


*Programação Paralela com MPI*


## Programação Paralela

Existem várias aplicações computacionais que podem ser divididas em sub-tarefas independentes, que podem ser executadas simultaneamente em máquinas paralelas (AUDE, 1998, p.73). A programação paralela permite que sejam utilizados os diversos módulos de processamentos de máquinas paralelas para se executar tais aplicações.

As máquinas paralelas podem ser divididas em dois grupos: máquinas com memória primária fisicamente compartilhada, conhecidas como multiprocessadores e máquinas com memória distribuída, conhecidas como multicomputadores. Por outro lado, existem dois modelos de programação, que determinam se a memória é logicamente compartilhada ou não. No primeiro modelo, a comunicação entre as tarefas pode ser feita utilizando-se variáveis compartilhadas entre as mesmas. No segundo modelo de programação, a comunicação é feita através de troca de mensagens. Estas duas classificações – memória fisicamente compartilhada ou não e memória logicamente compartilhada ou não – são ortogonais (ANDREW S. TANENBAUM, 1999, p.526).

Existem diversos ambientes de programação paralela que visam auxiliar o
desenvolvimento de aplicações que exploram os recursos de máquinas paralelas.
Dentre os diversos ambientes de programação paralela, destaca-se o MPI (SNIR, 1996;
MPI FORUM, 1995), por ter se tornado um padrão de facto para qualquer tipo de
máquina paralela. O MPI (Message Passing Interface) é uma especificação de uma
biblioteca para programação paralela usando troca de mensagens. Esta especificação
permite que sejam desenvolvidas implementações do MPI para qualquer tipo de
máquina paralela e, ao mesmo tempo, que estas implementações possam aproveitar da
melhor forma os recursos de cada tipo de máquina.


## O Ambiente MPI

Este capítulo apresenta a especificação da interface padrão para troca de mensagens – o MPI –, enumerando seus principais objetivos e comentando sobre suas versões. Em seguida, são descritos os conceitos básicos do MPI, bem como um pequeno exemplo para que se tenha uma familiarização rápida com o ambiente MPI. Finalmente, são
descritas as suas principais operações de comunicação ponto-a-ponto e coletiva.


### Apresentação do MPI

MPI (Message Passing Interface) é uma biblioteca de funções padrão e portátil, que
define a sintaxe e a semântica de um núcleo de rotinas útil para se escrever programas
que exploram a existência de múltiplos processadores com troca de mensagem (PETER
PACHECO, 1998, p.3).
Segundo (SNIR, 1996, p.xi): “O padrão MPI é o resultado de um esforço que envolveu
mais de 80 pessoas de 40 organizações, principalmente dos Estados Unidos e Europa. A
maioria dos maiores vendedores de computadores concorrentes da época estava
envolvida com o MPI, bem como pesquisadores de universidades, de laboratórios do
governo e da indústria”.
Este grupo, que definiu o MPI, passou a se chamar MPI Forum (MPI-FORUM) e é
responsável pela manutenção deste padrão.


### Objetivos

Os principais objetivos do MPI são:
 - Permitir que sejam desenvolvidas implementações da especificação MPI em
máquinas com arquiteturas diferentes. A partir do mesmo código fonte, que utiliza o
MPI, pode-se gerar um programa que pode ser executado em multicomputadores
com memória distribuída, em multiprocessadores com memória compartilhada, em
clusters de estações de trabalho – COWs (Clusters of Workstations) – e em uma combinação destes tipos de máquinas – ambientes heterogêneos – desde que haja
uma implementação da biblioteca MPI para a plataforma específica.

 - Permitir uma implementação eficiente de comunicação:
    - evitando, quando possível, cópia de memória para memória,
    - permitindo sobreposição de comunicação e computação.

 - Prover uma semântica de interface que seja independente de linguagem de
programação. Existem implementações de MPI que podem ser usadas por
programas escritos nas linguagens C, C++ e Fortran.

 - Prover uma interface de comunicação confiável. Falhas de comunicação devem ser
tratadas pelo subsistema de comunicação da plataforma.

 - Definir uma interface familiar para os usuários dos sistemas de troca de mensagens
mais comuns como por exemplo: PVM (GEIST, 1994) e P4 (BUTLER, 1992).

 - Projetar uma interface que permita thread-safety, ou seja, que permita que as
funções possam ser invocadas de forma segura por múltiplas threads
concorrentemente (ROBBINS, 1996, p.23).


### Versões

A primeira versão do MPI, chamada MPI-1.0, foi lançada em 1994 pelo MPI Forum.
Em 1995, foi disponibilizada outra versão, a MPI-1.1, sobre a qual este trabalho se
baseia (MPI FORUM, 1995; GROPP, 1996).

Posteriormente, foi lançada a versão MPI-2, que consiste de extensões à versão anterior.
Nestas extensões estão incluídas operações não existentes nas anteriores como, por
exemplo: operações para criação e gerenciamento de processos, entrada e saída paralela
e operações para acesso remoto à memória (GROPP, 1999, p.4).

MPI-3.1 foi aprovada pelo MPI Forum em junho de 2015.



## Conceitos Básicos em MPI

### Tarefas e Communicators

Um programa MPI consiste de várias tarefas autônomas, que executam seu próprio
fluxo de instruções, podendo ser classificado, portanto, como sendo um programa
MIMD (multiple instruction multiple data), segundo a taxonomia de Flynn (FLYNN,
1972). As tarefas se comunicam através de chamadas às primitivas de comunicação do
MPI.

Todas as rotinas do MPI relacionadas à comunicação entre tarefas possuem como
parâmetro um communicator, que é uma estrutura de dados que representa um conjunto
ordenado de tarefas que podem trocar mensagens entre si. Portanto, esta estrutura de
dados representa o domínio da comunicação.

Toda tarefa MPI pertence a pelo menos um communicator e possui, para cada
communicator, um rank, que é a sua identificação unívoca no mesmo. Os valores dos
ranks são números inteiros consecutivos que variam de 0 até o número de tarefas do
communicator menos 1.

Todo par (communicator, rank) identifica apenas uma tarefa em um programa MPI.



### Comunicação por Passagem de Mensagem

Existem dois tipos de comunicação por passagem de mensagem: a comunicação ponto-
a-ponto, que consiste na transmissão de dados entre um par de tarefas, uma delas
enviando e a outra recebendo e a coletiva, que é usada para se transmitir dados entre
todas as tarefas de um mesmo grupo especificado por um communicator.

A figura que se segue ilustra, de forma simplificada, um exemplo de comunicação
ponto-a-ponto em duas etapas. Na primeira etapa, a tarefa emissora coloca a mensagem
no seu buffer de envio e a tarefa receptora possui um buffer de recepção cujo conteúdo é
inválido neste momento. Na segunda etapa, a mensagem é copiada para o buffer de
recepção. Esta cópia pode ser feita de duas formas: diretamente do buffer de envio para
o buffer de recepção (representado pela seta contínua), ou indiretamente, sendo copiada
para um ou mais buffers temporários antes de ser copiada para o buffer de recepção
(representado pelas setas pontilhadas).



### Tipos de chamadas MPI

Os seguintes termos são usados para se discutir as rotinas do MPI:
 - local: se a conclusão de uma rotina depender somente da tarefa local que está em
execução. Tal operação não requer uma comunicação explícita com outra tarefa do
usuário.
 - não-local: se a conclusão da rotina necessitar da execução de alguma rotina MPI em
outra tarefa.
 - bloqueante: se a rotina não retorna enquanto não for permitido ao usuário reutilizar
os recursos especificados na chamada da mesma. Por exemplo, uma rotina de envio
bloqueante não retorna até que o buffer de envio tenha sido copiado para outro
lugar, de modo que o emissor fique livre para alterá-lo.
 - não-bloqueante: se a rotina puder retornar antes que a operação iniciada pela mesma
conclua. Neste caso, não será permitido ao usuário reutilizar os recursos (como
buffers) especificados na chamada. Uma chamada a uma rotina não-bloqueante pode
iniciar alterações no estado da tarefa chamadora que ocorrem depois que a chamada
retorna. Por exemplo, uma chamada não-bloqueante pode iniciar uma operação de
recepção, mas a mensagem é realmente recebida após o retorno da rotina.
 - coletiva: se todas as tarefas em um grupo de tarefas precisarem invocar a rotina.


### Primeiro exemplo

Como primeiro exemplo, é apresentado um programa simples que usa a biblioteca MPI.
O objetivo deste programa é fazer com que cada tarefa cujo rank é diferente de 0 envie
uma mensagem para a tarefa cujo rank é 0. A tarefa 0, por sua vez, exibe as mensagens
recebidas. Todas as tarefas pertencem a um único communicator: MPI_COMM_WORLD.

```c
#include <stdio.h>
#include <mpi.h>

#define MAXLEN 100

main(int argc, char** argv) {
	int myRank;
	/* rank da tarefa */
	int n;
	/* numero de tarefas */
	int source;
	/* rank da origem */
	int dest;
	/* rank do destino */
	int tag = 1;
	/* tag para as mensagens */
	char message[MAXLEN];
	/* buffer para a mensagem */
	MPI_Status status;
	/* status de retorno para o receptor */
	MPI_Init(&argc, &argv);
	MPI_Comm_rank(MPI_COMM_WORLD, &myRank);
	MPI_Comm_size(MPI_COMM_WORLD, &n);
}
if(myRank != 0) {
dest = 0;
sprintf(message, "Alo! Da tarefa %d!", myRank);
MPI_Send(message, strlen(message)+1, MPI_CHAR, dest,
tag, MPI_COMM_WORLD);
} else {
for(source = 1; source < n; source++) {
MPI_Recv(message, MAXLEN, MPI_CHAR, source, tag,
MPI_COMM_WORLD, &status);
printf("%s\n", message);
}
}
MPI_Finalize();
```

... trabalho em progresso.


## Mini-biografia

Analista de Sistemas no SERPRO (Serviço Federal de Processamento de Dados), desde 2005. Mestre em Informática pela UFRJ (Universidade Federal do Rio de Janeiro) - NCE (Núcleo de Computação Eletrônica) - IM (Instituto de Matemática), em Arquitetura de Computadores / Processamento Paralelo. Bacharel em Ciência da Computação pela PUC (Pontifícia Universidade Católica) Minas Gerais. Professor Universitário. Sítio: http://bit.ly/sidneybf.

## Referência Bibliográfica



