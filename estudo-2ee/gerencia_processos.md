# Gerencia de processos
---

## Criação de Processos

Na criação de processos, um processo criador (chamado de pai) gera novos
processos (chamados filhos), formando uma grande estrutura de árvore no sistema.

Para que esse novo processo filho funcione, ele precisa de recursos do sistema,
como tempo de CPU, memória e arquivos. O sistema operacional lida com esse
compartilhamento de três formas possíveis:

- O pai e os filhos compartilham todos os recursos
- Os filhos compartilham apenas um subconjunto dos recursos do pai
- O pai e o filho não compartilham recurso algum

Já em relação à execução, existem dois caminhos: ou o pai continua rodando ao
mesmo tempo (concorrentemente) que o filho, ou o pai pausa sua própria execução
e espera até que o filho termine a tarefa dele. Em sistemas UNIX, por exemplo, a
criação desse novo processo é feita através de uma chamada de sistema chamada
fork. 

## Término de processo

Um processo termina naturalmente quando executa sua última instrução e pede ao
sistema operacional para ser finalizado através da chamada de sistema exit().
Nesse momento, ele pode enviar dados de retorno ao processo pai (através da
operação wait()) e o sistema operacional liberar todos os recursos que ele
ocupava, como memória física e virtual, arquivos abertos e buffers de E/S

Porém, um porcesso pai também pode forçar o término de um processo filho usando
uma chamada como o abort(). Essa permissão é restrita ao pai para evitar que
usuários fechem processos uns dos outros de forma aleatória. O pai geralmente
interrompe o filho por três motivos 27principais:

1. O filho excedeu o uso dos recursos que foram alocados para ele
2. A tarefa que o filho estava executando não é mais necessária
3. O próprio processo pai está sendo encerrado. Em alguns sistemas, isso força
   um término em cascata, onde todos os filhos morrem junto com o pai

## Processos Cooperativos
Processos cooperativos são aqueles que podem afetar ou ser afetados pela excução
de outros processos no sistema, o que normalmente acontece porque eles
compartilham dados. Eles são o oposto dos processos independentes, que rodam
totalmente isolados.

Trabalhar de forma cooperativa traz quatro vantagens:

- Compartilhamento de informações: permite que vários processos acessem o mesmo
  recurso concorrentemente, como um arquivo compartilhado
- Agilidade na computação: uma tarefa grande pode ser quebrada em subtarefas
  para rodarem em paralelo, ganhando velocidade
- modularidade: facilita a construção do sistema, dividindo as funções em
  processos separados
- conveniência: Permite que um mesmo usuário faça várias coisa simultaneamente,
  como editar, imprimir e compilar um código. 

## Problema Produtor-Consumidor

O problema produtor-consumidor é o exemplo clássico que ilustra como processos
cooperativos trabalham juntos.

A dinâmica é direta: um processo, chamado de produtor, fica responsável por
gerar dados ou informações, enquanto um segundo processo, chamado consumidor,
acessa e consome esses dados.

Para conseguirem trocar essas informações sem que um atropele o outro, eles
utilizam uma área de memória compartilhada que funciona como uma fila, chamada
de buffer. Esse buffer pode existir de duas formas:

- ilimitado: não possui um limite de tamanho prático, o que significa que o
  produtor pode gerar e colocar dados na fila sem nunca precisar esperar
- limitado: a fila possui um tamanho fixo. Se ela encher, o produtor é obrigado
  a pausar e esperar o consumidor retirar algo para liberar espaço.

## Comunicação entre processos

A comunicação Interprocessos (IPC) é o mecanismo que permite que os processos
troquem dados e sincronizem suas tarefas sem precisarem usar variáveis
compartilhadas na memória.

Para conversarem, os processos estabelecem um enlade ce comunicação e utilizam
duas operações báscias: send e receive

Essa troca ocorre de duas maneiras principais:

- Síncrona (bloqueante): O processo que envia a mensagem fica travado esperando
  até que o destino receba o aviso e leia a mensagem
- Assíncrona: O processo despacha a mensagem (que fica guardada em um buffer
  local) e continua executando seu código livremente, em paralelo, sem precisar
  esperar o outro.

Para que a comunicação funcione sem interrupções, o sistema organiza essas
mensagens em Buffers (filas de mensagens)

## Capacidade dos buffers

As três capacidades dos buffers definem como as filas de mensagem funcionam
durante a comunicação:

- capacidade zero: A fila guarda nenhuma mensagem. O emissor precisa pausar e
  entregar a mensagem diretamente para o receptor no exato momento em que ele
  estiver pronto, o que é chamado de rendezvous (encontro)
- capacidade limitada: A fila tem um tamanho exato de espaço para n mensagens. O
  emissor só precisa esperar e parar de enviar se a fila ficar completamente
  cheia
- capacidade ilimitada: A fila tem tamanho infinito. O processo emissor pode
  mandar mensagens sem parar e nunca precisa esperar.

## Remote Procedure Call (RPC) e Remote Method Invocation (Java)

O RPC (Remote Procedure Call) e o RMI (Remote Method Invocation) são técnicas para que processos em máquinas diferentes conversem pela rede como se estivessem rodando no mesmo computador.

- RPC: Ele abstrai a chamada de uma função através da rede. Para esconder a complexidade, ele usa um intermediário chamado "stub". O stub no cliente empacota os parâmetros da requisição e a envia. O stub no servidor recebe a mensagem, desempacota os dados e aciona o procedimento real por lá. 

- RMI: É basicamente a versão do RPC criada especificamente para Java e adaptada para a programação orientada a objetos. Em vez de chamar uma função solta, o RMI permite que um programa em uma máquina invoque diretamente um método de um objeto que está rodando remotamente em outra Máquina Virtual Java (JVM).

