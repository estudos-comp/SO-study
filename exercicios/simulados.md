
## **Prova 1: Fundamentos de Hardware e Conceitos Iniciais de S.O.**

#### **UNIVERSIDADE DE PERNAMBUCO - Escola Politécnica (UPE-POLI)**
#### **Disciplina:** Sistemas Operacionais

**1) (1,5 pt) Assinale a alternativa incorreta sobre a evolução e os tipos de Sistemas Operacionais:**

* A) O grande gargalo e responsável pela ociosidade da CPU sempre foram as operações de entrada e saída, especialmente na segunda fase da evolução histórica dos SOs.


* B) Os sistemas operacionais de tempo compartilhado se assemelham aos sistemas de multitarefas cooperativas em que cada job que executa na CPU passa o controle para o próximo.


* C) A multiprogramação foi uma técnica introduzida com o objetivo principal de minimizar a ociosidade da CPU.


* D) Seguindo a evolução histórica dos sistemas operacionais, a primeira fase foi marcada pelos computadores compostos de válvulas e painéis.



**2) (2,0 pt) Sobre a arquitetura de processadores e execução de instruções:**
Descreva como um processador faz para controlar e executar instruções presentes na memória principal, detalhando a atuação de cada um dos seus componentes. Na sua explicação, inclua como se comunicam e para que servem os registradores MAR e MBR.

**3) (1,5 pt) O acesso direto à memória (DMA) é usado em dispositivos de I/O de alta velocidade.**
Responda: Como a CPU se relaciona com o dispositivo para coordenar a transferência de dados e como ela sabe quando as operações na memória foram concluídas? 

**4) (1,0 pt) Assinale a alternativa correta em relação aos componentes de hardware:**

* A) A CPU ou processador é formada por unidade de controle, unidade lógica e aritmética e registradores, sendo a unidade lógica e aritmética a única responsável pela busca e execução de instruções na memória.


* B) O objetivo principal da memória cache é minimizar a disparidade entre a velocidade com que o processador executa instruções e a velocidade com que dados são lidos e gravados na memória principal.


* C) Pipelining é uma técnica que permite o processador executar múltiplas instruções de forma estritamente sequencial, aguardando o término de uma para iniciar a busca da próxima.


* D) Toda vez que o processador faz referência a um dado que se encontra na memória, a memória cache só é verificada primeiramente em caso de cache hit.



**5) (1,0 pt) Interrupções e Exceções:**
Quais são as diferenças entre uma exceção e uma interrupção? As exceções podem ser geradas intencionalmente por um programa de usuário? Caso possam, com que finalidade? 

[RESOLUÇÃO](resolucao/prova-1.md)

---

## **Prova 2: Gerenciamento de Processos e Escalonamento**

#### **UNIVERSIDADE DE PERNAMBUCO - Escola Politécnica (UPE-POLI)**
#### **Disciplina:** Sistemas Operacionais

**1) (2,0 pt) Considerando o ciclo de vida de um processo (admissão, fila dos prontos, execução na UCP, fila dos bloqueados, liberação):**
Qual o papel de um dispatcher e o que ele faz? Além disso, explique o que determina um processo sair da CPU e ir para a fila dos bloqueados.

**2) (1,5 pt) Assinale a alternativa incorreta sobre políticas de escalonamento:**

* A) No escalonamento por prioridades, atribui-se a processos de Entrada/Saída a prioridade máxima, sendo a fração do último quantum que o processo usou um fator decisivo.


* B) No algoritmo Round-robin, a cada processo é atribuído um intervalo de tempo ou quantum para uso da CPU.
* C) Uma das funções do escalonador de memória é decidir quais jobs são levados para o disco em uma operação de swap out.


* D) O escalonamento preemptivo ocorre apenas quando o processo usa todo o seu quantum, momento em que ele é colocado no final da fila de bloqueados.

**3) (1,5 pt) Comunicação Inter-processos (IPC):**
Quais os tipos específicos de comunicação inter-processos que podem haver e o que caracteriza cada uma delas (síncrona vs assíncrona)? 

**4) (1,0 pt) Políticas para Sistemas em Lote:**
Cite e defina pelo menos 3 possíveis algoritmos que podem existir numa política de escalonamento para sistemas em lote.

**5) (1,0 pt) System Calls:**
Defina e diga para que serve uma system call. Esquematize o passo a passo que deve ser executado quando uma system call é chamada a partir de um programa.

[RESOLUÇÃO](resolucao/prova-2.md)

---

## **Prova 3: Gerenciamento de Memória (Alocação, Paginação e Segmentação)**

#### **UNIVERSIDADE DE PERNAMBUCO - Escola Politécnica (UPE-POLI)**
#### **Disciplina:** Sistemas Operacionais

**1) (1,5 pt) Assinale a alternativa incorreta no contexto de gerenciamento de memória:**

* A) As duas principais técnicas de gerenciamento de memória virtual são paginação e segmentação.


* B) A fragmentação externa ocorre quando há o espaço de memória total suficiente para satisfazer a uma requisição, mas ele não é contíguo.


* C) O espaço de endereços lógicos de um processo precisa ser obrigatoriamente contíguo para que o sistema operacional consiga mapeá-lo na memória física.


* D) Um processo pode ser retirado (swapped-out) temporariamente da memória física para um disco e, posteriormente, trazido de volta para continuar sua execução.



**2) (1,5 pt) Memória Associativa:**
Explique o que seria uma TLB ou memória associativa e a motivação de sua existência no contexto da tradução de endereços.

**3) (1,5 pt) Assinale a alternativa incorreta sobre a técnica de Segmentação:**

* A) Na segmentação, um programa é visto como um conjunto de segmentos, onde cada segmento é uma unidade lógica como um programa principal, procedimento ou função.


* B) Cada entrada da tabela de segmentos especifica o endereço físico inicial onde o segmento reside na memória e a extensão (tamanho) desse segmento.


* C) A fragmentação interna é um dos principais problemas de alocação gerados exclusivamente pela técnica de segmentação.


* D) Nessa técnica, o programador precisa estar ciente de que a segmentação está sendo utilizada para organizar o código.



**4) (1,5 pt) Proteção de Memória:**
Descreva um mecanismo que garantiria a proteção da memória impedindo que um programa modificasse a memória associada a outros programas concorrentes.

**5) (1,0 pt) Endereçamento:**
Explique o que significa uma memória principal com 64kbytes. Caracterize-a em termos de quantidade de células, assumindo que cada uma representa um endereço de memória com capacidade de armazenamento de 8 bits.

[RESOLUÇÃO](resolucao/prova-3.md)

---

## **Prova 4: Memória Virtual e Impasses (Deadlocks)**

#### **UNIVERSIDADE DE PERNAMBUCO - Escola Politécnica (UPE-POLI)**
#### **Disciplina:** Sistemas Operacionais

**1) (2,0 pt) Algoritmos de Substituição de Páginas:**
Cite e defina os 3 principais algoritmos de substituição de páginas abordados em sala e seus respectivos critérios para substituição das páginas.

**2) (2,0 pt) Desempenho e Localidade:**
O que é o princípio da localidade? Como o sistema operacional pode atuar para se aproveitar do mesmo no contexto de hierarquia de memória e memória virtual?

**3) (1,0 pt) Assinale a alternativa correta:**

* A) No carregamento dinâmico, a rotina é carregada na memória física antes mesmo de ser chamada, para garantir a velocidade de execução.


* B) Na técnica de overlay, o projeto de programação da estrutura é simples e gerido unicamente pelo Garbage Collector da linguagem de programação.


* C) Na alocação de múltipla partição, o algoritmo worst fit vai alocar o processo na pior partição, ou seja, aquela correspondente ao menor tamanho disponível.


* D) Na técnica de segmentação com paginação, os descritores de segmentos apontam para tabelas de páginas, unindo as vantagens de ambas as abordagens.

**4) (1,0 pt) Dispositivos de E/S:**
Cite e exemplifique as 2 principais categorias de dispositivos de entrada e saída, relacionando-os com a necessidade de memórias secundárias (como HDs).

**5) (1,0 pt) Terminação de Processos:**
Sobre gerenciamento de processos, explique as possíveis (e/ou diferentes) maneiras que um processo termina ou é finalizado e as providências que o S.O. toma em relação aos recursos.

[RESOLUÇÃO](resolucao/prova-4.md)

---

## **Prova 5: Exame Final (Revisão Geral S.O. e Arquitetura)**

#### **UNIVERSIDADE DE PERNAMBUCO - Escola Politécnica (UPE-POLI)**
#### **Disciplina:** Sistemas Operacionais

**1) (1,5 pt) Objetivos do S.O.:**
Os serviços e funções fornecidos por um sistema operacional podem ser divididos em categorias principais. Descreva pelo menos 3 metas/objetivos de um sistema operacional na sua função de Gerenciador de Recursos e 3 metas na sua função de Máquina Virtual.

**2) (1,5 pt) Arquitetura Multiprocessada:**
Descreva as diferenças estruturais e operacionais entre os multiprocessamentos simétrico e assimétrico. Em seguida, cite três vantagens e uma desvantagem de sistemas multiprocessadores.

**3) (1,5 pt) Caches e Hierarquia:**
Cite duas razões da utilidade das memórias caches. Que problemas elas resolvem e que problemas elas causam? Se um cache puder ser tão amplo quanto o dispositivo para o qual ele está armazenando, por que não dar a ele esse espaço e eliminar o dispositivo mais lento?.

**4) (1,5 pt) Assinale a alternativa incorreta:**

* A) Há registradores que armazenam informações de uso específico, como é o caso do PC e PSW. O PSW contém o endereço da próxima instrução que o processador deve buscar e executar.


* B) Se uma aplicação puder acessar o núcleo livremente, esta não pode alterar sua integridade, pois as implementações de segurança de um SO independem do hardware dos processadores.


* C) O escalonamento de tempo real se destaca pelo rigor no tempo de resposta imediato aos processos críticos.
* D) As alternativas A e B estão incorretas.

**5) (1,0 pt) Barramentos:**
Descreva os barramentos, suas funções no tráfego de dados entre processador, memória e periféricos, e explique brevemente a sua evolução tecnológica.

Entendido! Se o padrão oficial da professora Tarciana é cobrar 10 questões por prova, vamos ajustar a nossa simulação para refletir exatamente essa estrutura. A prova abaixo foi desenhada balanceando questões de múltipla escolha (pedindo a incorreta, como é comum no estilo dela) e questões discursivas esquemáticas, cobrindo desde a arquitetura de hardware até o gerenciamento de memória e impasses.

[RESOLUÇÃO](resolucao/prova-5.md)

---

## **UNIVERSIDADE DE PERNAMBUCO - Escola Politécnica (UPE-POLI)**

#### **Curso:** Engenharia da Computação
#### **Disciplina:** Sistemas Operacionais
#### **Professor(a):** Tarciana Dias da Silva

**ATENÇÃO:** A avaliação deverá ser respondida à caneta. Leia atentamente as questões de múltipla escolha, prestando atenção ao que se pede (correta ou incorreta).

**1) (1,0 pt) Sobre os conceitos iniciais e tipos de Sistemas Operacionais, assinale a alternativa incorreta:**

* A) Os serviços fornecidos por um SO podem ser divididos na visão de Gerenciador de Recursos (focado em eficiência e controle de hardware) e na visão de Máquina Virtual (focada em abstração e facilidade de uso para o programador).


* B) Sistemas de processamento em lote (Batch) processam programas agrupados sem a necessidade de interação direta do usuário durante a execução.


* C) Em sistemas operacionais de tempo compartilhado (timesharing), cada processo possui um tempo determinado (time-slice ou quantum) para uso da CPU, criando a ilusão de execução simultânea.
* D) A principal diferença entre sistemas fortemente acoplados (paralelos) e fracamente acoplados (distribuídos) é que os distribuídos compartilham a mesma memória principal e o mesmo relógio.

**2) (1,0 pt) Arquitetura e Execução na CPU:**
Descreva como um processador faz para controlar e executar instruções presentes na memória principal. Na sua explicação, detalhe a função dos registradores PC (Program Counter), PSW (Program Status Word), MAR e MBR, explicando como eles se comunicam.

**3) (1,0 pt) Multiprocessamento:**
Descreva as diferenças principais entre os multiprocessamentos simétrico (SMP) e assimétrico (ASMP). Em seguida, cite pelo menos duas vantagens e uma desvantagem de sistemas multiprocessadores.

**4) (1,0 pt) E/S e Acesso Direto à Memória (DMA):**
O acesso direto à memória (DMA) é usado em dispositivos de I/O de alta velocidade para impedir o aumento da carga de execução da CPU. Como a CPU se relaciona com o dispositivo para coordenar a transferência e como a CPU sabe quando as operações de cópia para a memória foram concluídas?

**5) (1,0 pt) Chamadas de Sistema (System Calls) e Processos:**
Defina e diga para que serve uma *system call*. Esquematize o passo-a-passo que deve ser executado quando uma system call é chamada a partir de um programa de usuário. Como essa chamada pode levar o processo a sair do estado de "execução" e ir para a "fila de bloqueados"? 

**6) (1,0 pt) No que concerne a políticas de escalonamento de processos, assinale a alternativa incorreta:**

* A) No algoritmo Round-Robin, a cada processo é atribuído um intervalo de tempo (quantum). Se o processo não terminar dentro desse tempo, ele sofre preempção.
* B) O algoritmo FIFO (First-In, First-Out) é estritamente não-preemptivo, o que significa que um processo só libera a CPU quando termina sua execução ou solicita uma operação de I/O.
* C) Escalonamento por prioridades pode sofrer do problema de *starvation* (inanição), que geralmente é resolvido pela técnica de *aging* (envelhecimento), aumentando a prioridade de processos que esperam há muito tempo.
* D) No escalonamento preemptivo, quando o processo usa todo o seu quantum, ele é colocado obrigatoriamente na fila de bloqueados, aguardando uma interrupção de hardware para voltar à fila de prontos.

**7) (1,0 pt) Comunicação Inter-processos (IPC):**
Quais os tipos específicos de comunicação inter-processos que podem haver e o que caracteriza cada uma delas (explique a diferença entre a comunicação síncrona e a assíncrona)?

**8) (1,0 pt) Assinale a alternativa incorreta no contexto de gerenciamento de memória:**

* A) As duas principais técnicas de gerenciamento de memória virtual são paginação e segmentação.


* B) A fragmentação externa ocorre quando há o espaço de memória total suficiente para satisfazer a uma requisição, mas ele não é contíguo.


* C) Na técnica de paginação, o espaço de endereços lógicos de um processo precisa ser obrigatoriamente contíguo para ser mapeado nos *frames* da memória física.


* D) Na segmentação, um programa é visto como um conjunto de segmentos, que representam unidades lógicas (como função, método, pilha, arrays).



**9) (1,0 pt) Memória Associativa e Desempenho:**
Explique o que seria uma TLB (Translation Lookaside Buffer) ou memória associativa e a motivação de sua existência no esquema de paginação. Relacione a utilidade da TLB com o "Princípio da Localidade".

**10) (1,0 pt) Substituição de Páginas:**
Cite e defina os 3 principais algoritmos de substituição de páginas abordados na disciplina (por exemplo: FIFO, LRU, Ótimo) e os seus respectivos critérios para decidir qual página será retirada da memória física.

[RESOLUÇÃO](resolucao/prova-6.md)

---

## **UNIVERSIDADE DE PERNAMBUCO - Escola Politécnica (UPE-POLI)**

#### **Curso:** Engenharia da Computação
#### **Disciplina:** Sistemas Operacionais
#### **Professor(a):** Tarciana Dias da Silva

**ATENÇÃO:**

1. Avaliação individual;
2. A avaliação deverá ser respondida à caneta;
3. Leia com atenção as questões de múltipla escolha para identificar o que se pede.

---

**1) (1 pt) Sobre a arquitetura de processadores e o ciclo de instrução, assinale a alternativa incorreta:**

* A) O PC (Program Counter) é o registrador responsável por armazenar o endereço da próxima instrução que o processador deve buscar e executar.
* B) O MAR (Memory Address Register) e o MBR (Memory Buffer Register) são registradores utilizados para auxiliar na leitura e escrita de/nas células da memória principal.


* C) Durante uma operação de leitura, a CPU armazena no MBR o endereço da célula a ser lida, e o dado lido é transferido da memória diretamente para o MAR.
* D) O PSW (Program Status Word) armazena informações sobre o estado atual da execução, como a ocorrência de *overflow*.



2) (1 pt) O acesso direto à memória (DMA) é usado em dispositivos de I/O de alta velocidade para impedir o aumento da carga de execução da CPU. A respeito desse mecanismo, responda:

* 
**a)** Como a CPU se relaciona com o dispositivo para coordenar a transferência? 


* 
**b)** Como a CPU sabe quando as operações da memória foram concluídas? 


* 
**c)** A CPU pode executar outros programas enquanto o controlador de DMA está transferindo dados. Esse processo interfere na execução dos programas de usuário? Caso interfira, que tipos de interferência são gerados? 



**3) (1 pt) Seguindo a evolução histórica e os tipos de sistemas operacionais, assinale a alternativa incorreta:**

* A) Os sistemas operacionais de tempo compartilhado (timesharing) surgiram para permitir que múltiplos usuários interagissem com o sistema simultaneamente, minimizando o tempo de resposta.


* B) A multiprogramação foi introduzida com o objetivo de minimizar a ociosidade da CPU, mantendo vários jobs na memória simultaneamente.


* C) Em um sistema *Batch* (lote), os programas são agrupados e processados sequencialmente, sendo altamente interativos e exigindo a constante intervenção do usuário durante a execução.


* D) Sistemas de tempo real possuem restrições rígidas de tempo, onde o não cumprimento de um prazo de resposta pode resultar em falha crítica do sistema.



**4) (1 pt) Considerando o esquema clássico de estados de um processo (admissão $\rightarrow$ fila dos prontos $\rightarrow$ execução na UCP $\rightarrow$ liberação/bloqueio), responda:**

* 
**a)** Qual o papel de um *dispatcher* e o que ele faz? 


* 
**b)** O que pode ocasionar um processo em execução na CPU ser pausado de forma preemptiva pelo sistema operacional? 


* 
**c)** O que determina um processo sair do estado de execução e ir para a fila dos bloqueados? 



**5) (1 pt) Assinale a alternativa incorreta no contexto de gerenciamento de memória:**

* A) A fragmentação externa ocorre quando há o espaço de memória total suficiente para satisfazer a uma requisição, mas ele não é contíguo.


* B) Na técnica de paginação, o espaço de endereços lógicos de um processo precisa ser contíguo, o que elimina totalmente o problema da fragmentação interna.
* C) Um processo pode ser retirado (*swapped-out*) temporariamente da memória para um armazenamento de apoio, para depois ser trazido de volta à memória a fim de continuar a execução.


* D) Na alocação de partição única, o esquema de registrador de base/relocação e limite é usado para proteger os processos do usuário uns dos outros e do sistema operacional.

**6) (1 pt) Sobre proteção e chamadas de sistema (System Calls), responda:**

* 
**a)** Defina o que é uma *system call* e explique para que ela serve na comunicação entre um programa de usuário e o SO.


* 
**b)** Descreva um mecanismo em nível de hardware/SO que garantiria a proteção da memória, impedindo que um programa modificasse a memória associada a outros programas concorrentes.



**7) (1 pt) No que concerne a políticas de escalonamento de processos, assinale a alternativa incorreta:**

* A) O algoritmo FIFO pode ou não causar a preempção do processo que está muito tempo usando a CPU.
* B) No algoritmo Round-robin, a cada processo é atribuído um intervalo de tempo ou *quantum* para execução.
* C) No escalonamento por prioridades, a inanição (*starvation*) de processos de baixa prioridade pode ser resolvida utilizando o mecanismo de *aging* (envelhecimento).
* D) Múltiplas filas de escalonamento permitem classificar processos (ex: interativos vs lote) e aplicar políticas diferentes para cada fila.

**8) (1 pt) No contexto de memória virtual, paginação e tradução de endereços, responda:**

* 
**a)** Explique o que seria uma TLB (Translation Lookaside Buffer) ou memória associativa e a principal motivação de sua existência.


* 
**b)** Cite e defina os 3 principais algoritmos abordados em sala para substituição de páginas quando a memória física (frames) está cheia.


* **c)** O que é o *Page Fault* (falta de página) e o que o SO deve fazer quando ele ocorre?

9) (1 pt) Qual é a finalidade das interrupções no funcionamento de um hardware computacional?  Assinale a afirmação incorreta:

* A) As exceções são eventos síncronos gerados pela execução de uma instrução específica pelo processador, como uma divisão por zero.
* B) As interrupções de hardware são eventos assíncronos gerados por dispositivos de E/S para sinalizar à CPU que precisam de atenção.
* C) As exceções nunca podem ser geradas intencionalmente por um programa de usuário, pois isso sempre resulta no encerramento forçado da aplicação (*abort*).
* D) O uso de interrupções é mais eficiente para o uso da CPU do que o método de *busy waiting* (espera ocupada).

**10) (1 pt) Sobre a organização e o número de processadores no sistema, responda:**

* 
**a)** Descreva as diferenças entre os multiprocessamentos simétrico (SMP) e assimétrico (ASMP).


* 
**b)** Cite três vantagens e uma desvantagem da utilização de sistemas multiprocessadores.

[RESOLUÇÃO](resolucao/prova-7.md)

--- 

## **UNIVERSIDADE DE PERNAMBUCO - Escola Politécnica (UPE-POLI)**

#### **Disciplina:** Sistemas Operacionais
#### **Simulado Temático:** Módulo 1 (Aulas 01, 02 e 03) - Fundamentos e Arquitetura

**1) (1 pt) A respeito da evolução histórica dos sistemas operacionais, assinale a alternativa incorreta:**

* A) A primeira fase (geração) foi marcada pelos computadores compostos de válvulas e painéis, onde não existia a figura do Sistema Operacional e a programação era feita fisicamente.
* B) O grande gargalo e responsável pela ociosidade da CPU na segunda geração foram as operações de entrada e saída, marcadas pela codificação em cartões perfurados.
* C) A técnica de multiprogramação foi desenvolvida com o objetivo primário de permitir que múltiplos usuários interagissem com o sistema simultaneamente através de terminais burros.
* D) O *Spooling* (Simultaneous Peripheral Operation On-Line) permitiu usar o disco como um buffer muito grande, lendo jobs de cartões para o disco assim que possível, desvinculando a CPU da velocidade dos periféricos mecânicos.

**2) (1 pt) Sobre a execução de instruções e os registradores da CPU, responda:**

* **a)** Qual a função do PC (Program Counter) e do IR (Instruction Register) durante o ciclo de busca e execução?S
* **b)** Como o MAR (Memory Address Register) e o MBR (Memory Buffer Register) interagem durante uma operação de escrita na memória?
* **c)** O que acontece com o conteúdo do PC após a busca de uma instrução?

**3) (1 pt) No contexto de interrupções e exceções, assinale a alternativa incorreta:**

* A) Interrupções são eventos assíncronos geralmente gerados por dispositivos de hardware, como controladores de E/S ou temporizadores (*clocks*).
* B) Uma exceção (ou *trap*) é uma interrupção gerada por software, causada por um erro (como divisão por zero) ou por uma solicitação específica de um programa de usuário.
* C) As exceções nunca podem ser geradas intencionalmente por um programa de usuário, sendo exclusivamente mecanismos de detecção de falhas críticas de hardware.
* D) Quando uma interrupção ocorre, o hardware salva o contexto atual (como o PC e registradores) para que o sistema operacional possa tratar o evento e, em seguida, retomar o processo de onde parou.

**4) (1 pt) O Acesso Direto à Memória (DMA) revolucionou o desempenho dos sistemas computacionais. A respeito dele, responda:**

* **a)** O que é o *Cycle Stealing* (roubo de ciclo) no contexto do DMA?
* **b)** Por que o uso de DMA é preferível à transferência de E/S programada (onde a CPU move cada byte) para dispositivos de alta velocidade?
* **c)** Em que momento exato o controlador de DMA aciona a CPU por meio de uma interrupção?

**5) (1 pt) Sobre os tipos de arquitetura e sistemas operacionais, assinale a alternativa incorreta:**

* A) Sistemas multiprocessadores simétricos (SMP) compartilham a mesma memória principal e são controlados por um único sistema operacional que distribui a carga entre as CPUs.
* B) Em sistemas fortemente acoplados (multiprocessadores), se uma CPU falhar, o sistema inteiro necessariamente entra em colapso, pois não há redundância de processamento.
* C) Sistemas operacionais distribuídos gerenciam um conjunto de computadores independentes (fracamente acoplados), mas apresentam aos usuários a ilusão de um sistema único.
* D) Sistemas operacionais de tempo real (*Real-Time*) são classificados em *Hard* e *Soft*, dependendo da tolerância do sistema ao atraso no cumprimento de prazos.

**6) (1 pt) A hierarquia de memória é fundamental para o desempenho do computador. Responda:**

* **a)** Defina o Princípio da Localidade (Espacial e Temporal).
* **b)** Cite duas razões para a utilidade das memórias caches na hierarquia. Que problemas elas resolvem?
* **c)** Se uma memória cache puder ter o mesmo tamanho do dispositivo secundário (como um HD), por que não eliminar o HD e usar apenas a cache?

**7) (1 pt) Sobre a proteção de hardware e o modo dual, assinale a alternativa incorreta:**

* A) O bit de modo (*mode bit*) é suportado pelo hardware para indicar o modo de operação atual: usuário (1) ou supervisor/kernel (0).
* B) Instruções privilegiadas, como o controle de interrupções e o acesso direto ao hardware de E/S, só podem ser executadas quando o sistema está em modo supervisor.
* C) Quando um programa de usuário chama uma *System Call*, ocorre uma mudança de contexto, mas o bit de modo permanece inalterado para garantir a segurança dos dados do usuário.
* D) O temporizador (*timer*) é um recurso de proteção que previne que um programa de usuário monopolize a CPU, gerando uma interrupção após um intervalo de tempo predefinido.

**8) (1 pt) Diferencie o paralelismo em nível de instrução, respondendo:**

* **a)** Como funciona a técnica de *Pipelining*?
* **b)** Qual a diferença fundamental entre uma arquitetura puramente com *Pipeline* e uma arquitetura *Superscalar*?
* **c)** Como os *pipelines* melhoram o *throughput* (vazão) do processador sem necessariamente reduzir o tempo de execução de uma única instrução individual?

**9) (1 pt) Assinale a alternativa incorreta a respeito de System Calls e do SO como Máquina Virtual:**

* A) A *System Call* é a interface entre um programa em execução e o sistema operacional.
* B) Do ponto de vista de "Máquina Virtual", o SO esconde a complexidade e os detalhes sujos do hardware, fornecendo ao programador um conjunto de instruções mais convenientes.
* C) As *System Calls* são implementadas como instruções comuns no nível de usuário, não requerendo nenhuma interrupção de software (trap) para serem acionadas.
* D) Passar parâmetros por registradores ou através de um bloco na memória (passando o endereço) são métodos comuns de envio de dados para uma *System Call*.

**10) (1 pt) Sobre Barramentos (Bus), responda:**

* **a)** Defina o que é um barramento de sistema e liste os três principais tipos de vias (linhas) que o compõem.
* **b)** Explique por que a arquitetura de barramento único tornou-se um gargalo para computadores modernos.
* **c)** Qual a solução arquitetural implementada para resolver o problema do barramento único?

[RESOLUÇÃO](resolucao/prova-8.md)

---

## **UNIVERSIDADE DE PERNAMBUCO - Escola Politécnica (UPE-POLI)**

#### **Disciplina:** Sistemas Operacionais
#### **Simulado Temático:** Módulo 2 - Processos, Threads e Escalonamento

**ATENÇÃO:**

1. Avaliação individual;
2. A avaliação deverá ser respondida à caneta;
3. Leia com atenção as questões de múltipla escolha para identificar o que se pede.

---

**1) (1 pt) O ciclo de vida de um processo é modelado através de diagramas de transição de estados. Sobre este tema, assinale a alternativa incorreta:**

* A) Um processo no estado "pronto" (*ready*) está totalmente carregado na memória principal, possuindo todos os recursos necessários para a sua execução, aguardando apenas que o *dispatcher* lhe atribua a CPU.
* B) A transição do estado "executando" (*running*) para "bloqueado" (*blocked*) ocorre exclusivamente quando o processo esgota a sua fatia de tempo (*quantum*) de uso da CPU.
* C) A transição de "executando" para "pronto" pode ocorrer devido a uma preempção por tempo, geralmente sinalizada por uma interrupção de relógio (*clock/timer*).
* D) Em modelos mais elaborados, a criação de um processo obriga-o a passar pelo estado "novo" (*new*), onde é admitido no sistema antes de ser transferido para a fila de prontos.

**2) (1 pt) A troca de contexto (*Context Switch*) é o mecanismo central que permite a multiprogramação e o tempo compartilhado. A respeito dela, responda:**

* **a)** O que é o Bloco de Controlo de Processo (PCB ou BCP) e qual é a sua utilidade no momento de uma troca de contexto?
* **b)** Descreva, passo a passo, o que o Sistema Operativo (com o auxílio do *hardware*) faz ao retirar o Processo A da execução e colocar o Processo B a executar.
* **c)** Por que razão a troca de contexto é considerada um *overhead* (trabalho administrativo/custo indireto) para o sistema computacional e não um "trabalho útil"?

**3) (1 pt) Relativamente ao conceito de *Threads* e à sua implementação (como abordado em Java na Aula 10), assinale a alternativa incorreta:**

* A) Em linguagens como Java, uma *Thread* pode ser instanciada implementando a interface `Runnable`, o que exige a sobrescrita (definição) obrigatória do método `run()`.
* B) Ao contrário de processos distintos que operam em isolamento, as *threads* pertencentes ao mesmo processo partilham o mesmo espaço de endereçamento de memória lógica e os mesmos ficheiros abertos.
* C) Uma grande vantagem prática do uso de *threads* é a economia de recursos, sendo a criação e a troca de contexto de uma *thread* significativamente mais "leves" e rápidas do que as de um processo pesado (*heavyweight process*).
* D) Todas as *threads* de um processo partilham obrigatoriamente a mesma Pilha de Execução (*Stack*) e o mesmo Contador de Programa (PC), de modo a garantirem o sincronismo perfeito das instruções.

**4) (1 pt) A criação de processos e as Chamadas ao Sistema (*System Calls*) caminham lado a lado no uso interativo do sistema operacional. Com base nisto, responda:**

* **a)** Quando um utilizador digita um comando num interpretador (*shell*), que Chamada de Sistema clássica do UNIX o *shell* invoca para duplicar-se e criar um processo filho?
* **b)** Durante a execução desse processo filho, caso ele necessite de realizar uma operação de I/O (Entrada/Saída), ele terá de mudar do "Modo Utilizador" para o "Modo *Kernel*". Qual a justificação técnica para a existência destes dois modos arquiteturais?
* **c)** O que acontece rotineiramente com o processo pai (o *shell*) após criar o processo filho, enquanto aguarda que este termine o seu trabalho (executando um `exit`)?

**5) (1 pt) No que diz respeito às características dos processos e aos algoritmos de escalonamento, assinale a alternativa incorreta:**

* A) O escalonamento *Round-Robin* (Chaveamento Circular) atribui um *quantum* de tempo igualitário a cada processo, sendo, por natureza, um modelo preemptivo.
* B) Processos *CPU-Bound* (limitados pela CPU) são aqueles que passam a maior parte do seu ciclo a executar operações matemáticas complexas, raramente necessitando de aceder a dispositivos de Entrada/Saída.
* C) Processos *I/O-Bound* (limitados por E/S) devem receber a menor prioridade no escalonador interativo, uma vez que monopolizariam a CPU à espera que o disco ou a rede respondessem, travando assim o sistema.
* D) O escalonamento baseado puramente em prioridades estáticas pode causar inanição (*starvation*), cenário em que processos de baixa prioridade aguardam indefinidamente pelo processador.

**6) (1 pt) O projeto de um algoritmo de escalonamento deve alinhar-se com os objetivos (metas) do ambiente. Sobre isto, elabore:**

* **a)** Identifique pelo menos três objetivos gerais que um bom algoritmo de escalonamento deve possuir.
* **b)** Num ambiente focado em sistemas de processamento em Lote (*Batch*), cite e defina dois algoritmos clássicos que poderiam ser utilizados (ex: FIFO/FCFS, SJF).
* **c)** Qual é a limitação fulcral do algoritmo FIFO num sistema interativo (Tempo Compartilhado)? Como é que o algoritmo *Round-Robin* resolve esse exato problema?

**7) (1 pt) Sobre Processos Cooperativos e o paradigma do Produtor-Consumidor (Aula 09), assinale a alternativa incorreta:**

* A) A divisão de funções complexas do sistema em processos paralelos (modularidade) é uma das grandes vantagens computacionais da cooperação de processos.
* B) No clássico problema do Produtor-Consumidor, a partilha de informações exige sincronização para prevenir a corrupção dos dados através de Condições de Corrida (*Race Conditions*).
* C) A implementação técnica de um *Buffer* Ilimitado (*Unbounded-buffer*) garante, na prática arquitetural de qualquer computador moderno, que o produtor nunca terá de ser suspenso por falta de endereços físicos para gravar novos dados.
* D) Em dispositivos como as impressoras, o recurso ao *Spool* permite que a exclusão mútua seja resolvida criando um único consumidor (um *daemon*) que recolhe os trabalhos produzidos pelos vários processos utilizadores.

**8) (1 pt) A parametrização matemática do tempo num S.O. de tempo compartilhado dita a perceção de desempenho dos utilizadores (Aula 05). Considere o escalonamento *Round-Robin*:**

* **a)** Suponha que a operação mecânica e administrativa de troca de contexto demore exatamente 1 milissegundo (ms). Se o *quantum* for parametrizado em 4 ms, qual será a percentagem do tempo da CPU desperdiçada (apenas no custo administrativo) de cada vez que ocorrer uma troca normal? (Explicite a lógica do seu cálculo).
* **b)** Se, de forma a melhorar a referida eficiência, parametrizarmos o *quantum* para 100 ms num cenário com dezenas de utilizadores concorrentes no servidor, que impacto direto o utilizador vai experienciar?
* **c)** Em suma, qual é a conclusão ("moral da história") a que o projetista do Sistema Operacional deve chegar ao escolher o tamanho ideal do *quantum*?

**9) (1 pt) Acerca de Impasses (*Deadlocks*), assinale a alternativa incorreta:**

* A) A condição de *Posse e Espera* postula que um processo já detém um recurso enquanto aguarda indefinidamente pela atribuição de um recurso adicional.
* B) A exclusão mútua num recurso não preemptível (ex: impressora ou gravador de CD) é uma condição necessária para que um *deadlock* ocorra.
* C) O *Algoritmo do Avestruz* é uma técnica computacional complexa onde o S.O. faz previsões futuras (baseadas no comportamento prévio do processo) para "enterrar" recursos inseguros no fundo da fila, prevenindo impasses lógicos absolutos.
* D) Uma das formas de recuperação num caso detetado de *deadlock* é de facto bastante agressiva: consiste na destruição (*kill* ou abort) forçada de um dos processos integrados no ciclo do impasse.

**10) (1 pt) Gestão de Múltiplas Filas e Interrupções no Sistema:**

* **a)** Como é que um S.O. moderno estrutura as filas para gerir processos com diferentes níveis de prioridade em relação à grande fila dos "Prontos" (*Ready*)?
* **b)** Quando o processo que está a ser executado invoca uma operação de I/O, para onde (qual estrutura do despachante) o S.O. o envia? Por qual entidade de hardware passa a aguardar?
* **c)** Assim que a operação do dispositivo estiver concluída e os dados estiverem disponíveis, que evento de arquitetura assíncrono comunica à CPU que ela deve acordar o processo? Qual o novo estado assumido pelo processo a partir desse instante?

[RESOLUÇÃO](resolucao/prova-9.md)

---

## **UNIVERSIDADE DE PERNAMBUCO - Escola Politécnica (UPE-POLI)**

#### **Disciplina:** Sistemas Operacionais
#### **Simulado Temático:** Módulo 3 (Aulas 06, 07 e 08) - Gerenciamento de Memória e Memória Virtual

**ATENÇÃO:**

1. Avaliação individual;
2. A avaliação deverá ser respondida à caneta;
3. Leia com atenção as questões de múltipla escolha para identificar o que se pede.

---

**1) (1 pt) O gerenciamento da memória principal (MP) passou por várias técnicas evolutivas. Sobre conceitos de alocação e fragmentação, assinale a alternativa incorreta:**

* A) A técnica de *Swapping* consiste em retirar um processo temporariamente da memória principal e movê-lo para o disco (armazenamento de apoio), trazendo-o de volta quando a UCP estiver disponível para ele.
* B) A fragmentação interna ocorre em sistemas com partições de tamanho fixo ou paginação, onde o espaço alocado para um processo é maior que o requisitado, gerando "sobras" inativas dentro do bloco.
* C) A fragmentação externa é resolvida de forma simples e direta pelo hardware, bastando que o disco mova fisicamente os processos a cada minuto para juntar os espaços livres em um grande bloco.
* D) Em alocação contígua, o particionamento dinâmico sofre severamente com o problema da fragmentação externa ao longo do tempo.

**2) (1 pt) Com o advento da Memória Virtual, o sistema operacional ganhou a capacidade de executar programas maiores que a memória física disponível. Sobre este tema, responda:**

* **a)** O que é o esquema de Paginação e como ele divide a Memória Lógica e a Memória Física? (Utilize os termos *páginas* e *frames/quadros*).
* **b)** Qual é a principal vantagem da paginação em relação ao problema da fragmentação externa?
* **c)** Onde fica armazenada a Tabela de Páginas de um processo e qual é a sua função exata na tradução de endereços?

**3) (1 pt) Sobre a técnica de Segmentação e sua diferença para a Paginação, assinale a alternativa incorreta:**

* A) A Segmentação apoia a visão que o desenvolvedor tem do seu programa (dividido em funções, pilhas, objetos e *arrays*), atribuindo tamanhos lógicos variáveis a cada segmento.
* B) Ao contrário da paginação, a segmentação pura não sofre com o problema da fragmentação externa, pois os segmentos podem se moldar perfeitamente a qualquer espaço residual na memória.
* C) Na segmentação, o endereço lógico é composto por um número de segmento e um deslocamento (*offset*) dentro desse segmento.
* D) É perfeitamente possível e comum (em arquiteturas como a da Intel) unir as duas técnicas na chamada Segmentação Paginada.

**4) (1 pt) Em um sistema de memória virtual com paginação sob demanda, o hardware desempenha um papel fundamental. Responda:**

* **a)** O que significa o bit de *válido/inválido* (v/i) associado a cada entrada na Tabela de Páginas?
* **b)** O que é o *Translation Lookaside Buffer* (TLB) e que problema de desempenho específico ele resolve na paginação?
* **c)** O que acontece com o tempo de acesso à memória se a TLB sofrer um *miss* (falha de busca)? Descreva os passos do hardware.

**5) (1 pt) Assinale a alternativa incorreta sobre o mecanismo de Page Fault (Falha de Página) (Aula 07):**

* A) Uma falha de página gera uma interrupção/exceção (trap) para o Sistema Operacional informando que o processo tentou acessar uma página que não está atualmente nos *frames* da memória física.
* B) Ao receber a interrupção de *Page Fault*, o Sistema Operacional aborta imediatamente o processo do usuário para evitar corrupção de memória.
* C) Durante o tratamento de uma falha de página genuína, o processo que causou a falha tem seu estado alterado para "bloqueado" enquanto aguarda o dado ser lido do disco.
* D) Ao finalizar a cópia da página do disco para o frame livre na RAM, o SO atualiza a tabela de páginas (bit válido) e reinicia a instrução que causou o erro.

**6) (1 pt) Descreva o tratamento de uma Falha de Página (*Page Fault*) a nível de Sistema Operacional, respondendo:**

* **a)** Se o SO percebe que não há nenhum *frame* (quadro) vazio na memória física para carregar a nova página, o que ele é obrigado a fazer?
* **b)** Como se dá a escolha da página que deverá sair da memória?
* **c)** Se a página escolhida para sair tiver sido modificada durante a sua estadia na memória RAM (*dirty bit* igual a 1), qual cuidado adicional o SO deve tomar antes de sobrescrevê-la?

**7) (1 pt) Sobre os Algoritmos de Substituição de Páginas abordados na Aula 08, assinale a alternativa incorreta:**

* A) O algoritmo *Ótimo* é amplamente implementado em todos os SOs comerciais (como Windows e Linux), pois ele prevê magicamente qual página demorará mais tempo para ser usada no futuro.
* B) O algoritmo FIFO (First-In, First-Out) é de fácil implementação, substituindo a página que foi trazida para a memória há mais tempo.
* C) O algoritmo LRU (*Least Recently Used*) baseia-se na ideia de que as páginas que não foram usadas recentemente provavelmente não serão usadas no futuro próximo (princípio da localidade).
* D) O objetivo principal de qualquer algoritmo de substituição de páginas é minimizar a taxa de falhas de página (*page fault rate*).

**8) (1 pt) A Anomalia de Belady é um fenômeno contraintuitivo na Teoria de Sistemas Operacionais. A respeito dela, responda:**

* **a)** O que dita o "senso comum" sobre a relação entre o número de *frames* físicos alocados a um processo e a sua quantidade de *page faults*?
* **b)** O que é, de fato, a Anomalia de Belady?
* **c)** Qual o algoritmo de substituição visto em sala de aula (Aula 08) que é expressamente suscetível a esta anomalia? Dê um motivo breve do porquê o LRU não sofre desse mal.

**9) (1 pt) Considere técnicas de gerência de memória mais simples que antecederam a memória virtual complexa. Assinale a alternativa incorreta:**

* A) A técnica de *Overlay* exige que o carregamento das partes do código (módulos que não são executados simultaneamente) seja implementado manualmente e de forma complexa pelo desenvolvedor do programa.
* B) No Carregamento Dinâmico, uma rotina (como tratamento de um erro raro) só é carregada na memória física quando é explicitamente chamada.
* C) Os registradores de Base e Limite são elementos lógicos programados no código-fonte das linguagens e executados inteiramente por software para proteger os acessos.
* D) O mapeamento de endereço Lógico para endereço Físico só acontece em tempo de execução na memória virtual moderna, necessitando de suporte via hardware (MMU).

**10) (1 pt) Para testar a eficiência de algoritmos de substituição, a professora frequentemente pede uma simulação de rastro (*trace*).** Considere uma RAM com apenas **3 frames livres** e a seguinte sequência de acesso a páginas (string de referência): `1, 2, 3, 4, 1, 2, 5, 1, 2, 3, 4, 5`.

* **a)** Quantas faltas de página ocorreriam utilizando o algoritmo FIFO puro? (Mostre o estado da memória).
* **b)** Se aumentássemos a RAM para **4 frames livres**, quantas faltas de página ocorreriam no mesmo algoritmo FIFO?
* **c)** O que o resultado obtido na comparação entre a) e b) ilustra de forma prática?

[RESOLUÇÃO](resolucao/prova-10.md)

---

## **UNIVERSIDADE DE PERNAMBUCO - Escola Politécnica (UPE-POLI)**

#### **Disciplina:** Sistemas Operacionais
#### **Simulado Temático:** Módulo 4 - Cálculos Práticos, Diagramas e Tópicos Avançados

**ATENÇÃO:**

1. Avaliação individual;
2. A avaliação deverá ser respondida à caneta;
3. Para as questões de cálculo, demonstre o seu raciocínio (ex: Gráfico de Gantt).

---

**1) (1 pt) Prática de Escalonamento de Processos (Aula 05):**
Considere o seguinte conjunto de processos, com a duração do pico de CPU (Burst Time) e o tempo de chegada dados em milissegundos:

| Processo | Tempo de Chegada | Tempo de Execução (Burst) |
| --- | --- | --- |
| P1 | 0 | 8 |
| P2 | 1 | 4 |
| P3 | 2 | 9 |
| P4 | 3 | 5 |

* **a)** Desenhe o Gráfico de Gantt e calcule o **Tempo Médio de Espera** (*Waiting Time*) considerando o algoritmo estritamente não-preemptivo **FCFS (FIFO)**.
* **b)** Desenhe o Gráfico de Gantt e calcule o **Tempo Médio de Retorno/Vida** (*Turnaround Time*) considerando o algoritmo não-preemptivo **SJF (Shortest Job First)**.

**2) (1 pt) Tradução Visual de Endereços na Paginação (Aula 07 e 08):**
Em provas passadas, a professora apresentou o diagrama de hardware de paginação. Descreva o passo a passo lógico desse diagrama respondendo:

* **a)** O endereço gerado pela CPU (Endereço Lógico) é dividido em duas partes: **p** e **d**. O que significa cada uma dessas letras?
* **b)** Como a Tabela de Páginas utiliza a variável **p** e o que ela devolve para o hardware (qual é a variável **f**)?
* **c)** Como o Endereço Físico final é montado para acessar a memória RAM antes de ser enviado ao barramento? O que acontece com a variável **d** nesse processo?

**3) (1 pt) Sobre os Modelos de Multithreading (Aula 10), assinale a alternativa incorreta:**

* A) No modelo *Many-to-One* (Muitos para Um), múltiplas threads de nível de usuário são mapeadas para uma única thread de kernel. A gerência das threads é feita no espaço do usuário, o que a torna eficiente.
* B) No modelo *Many-to-One*, se uma única thread de usuário fizer uma Chamada de Sistema (System Call) bloqueante (como ler um arquivo do disco), todo o processo será bloqueado, mesmo que outras threads estejam prontas para executar.
* C) O modelo *One-to-One* (Um para Um) mapeia cada thread de usuário para uma thread de kernel. Isso proporciona mais concorrência, pois permite que outra thread execute enquanto uma faz uma chamada bloqueante.
* D) Em processadores *multicore* modernos, o modelo *Many-to-One* é superior ao *One-to-One*, pois permite que as threads do usuário sejam executadas genuinamente em paralelo em múltiplos núcleos físicos, sem overhead de kernel.

**4) (1 pt) Superpaginação (Thrashing) e Desempenho (Aula 08):**
O *Thrashing* é um dos piores cenários de desempenho em um sistema de memória virtual.

* **a)** Defina o que é *Thrashing*. Como o tempo da CPU está sendo gasto quando o sistema entra nesse estado?
* **b)** Qual é a relação clássica entre o "Grau de Multiprogramação" (quantidade de processos na memória) e a utilização da CPU? O que acontece com a utilização da CPU no exato momento em que o *thrashing* se inicia?
* **c)** Como o Sistema Operacional deve agir, na prática, para recuperar um sistema que entrou em estado de *thrashing*?

**5) (1 pt) Assinale a alternativa incorreta sobre Grafos de Alocação de Recursos e Deadlocks (Aula 06):**

* A) Em um grafo de alocação, um círculo representa um processo e um quadrado/retângulo representa um tipo de recurso.
* B) Uma aresta (seta) direcionada do Processo para o Recurso ($Pi \rightarrow Rj$) é uma aresta de solicitação (o processo quer o recurso e está aguardando).
* C) Se um grafo de alocação de recursos não contém ciclos, então não existe deadlock no sistema.
* D) Se um grafo de alocação contém um ciclo, o sistema está, obrigatoriamente e matematicamente, em estado de deadlock, independentemente do número de instâncias que cada tipo de recurso possua.

**6) (1 pt) Avaliando Impasses por Grafo (Aula 06):**
Considere um sistema com dois processos ($P1$ e $P2$) e dois recursos de instância única ($R1$ e $R2$).

* **a)** Descreva a situação exata em que ocorreria um *Deadlock* (utilize as regras de retenção e solicitação entre eles).
* **b)** Se o Sistema Operacional utilizasse uma abordagem de Prevenção atacando a condição de "Espera Circular", como ele poderia forçar os processos a requisitar os recursos para garantir que o ciclo do item "a" nunca se formasse?

**7) (1 pt) Prática de Substituição de Páginas (Aula 08):**
Considere um processo que possui apenas **3 frames físicos** disponíveis na RAM. A sua execução gerou a seguinte string de referência de páginas lógicas: **`7, 0, 1, 2, 0, 3, 0, 4`**.

* **a)** Realize o teste de mesa e calcule o número total de Faltas de Página (*Page Faults*) utilizando o algoritmo **LRU (Least Recently Used)**.
* **b)** Realize o teste e calcule as falhas utilizando o algoritmo **ÓTIMO**.
* **c)** Por que o algoritmo Ótimo é impossível de ser implementado perfeitamente na prática em Sistemas Operacionais comerciais?

**8) (1 pt) No contexto de Alocação Contígua de Memória, assinale a alternativa incorreta:**

* A) O algoritmo *First-Fit* aloca o processo no primeiro buraco (vão) livre da memória que seja grande o suficiente para acomodá-lo, sendo geralmente mais rápido na busca.
* B) O algoritmo *Best-Fit* exige que a lista inteira de vãos livres seja percorrida (se não estiver ordenada) para encontrar o menor buraco que seja capaz de conter o processo.
* C) O algoritmo *Worst-Fit* aloca o processo no maior buraco disponível, o que, de forma contraintuitiva, sempre elimina o problema da fragmentação externa ao deixar sobras grandes e facilmente reutilizáveis.
* D) A compactação de memória é uma solução em tempo de execução para juntar todas as memórias livres em um grande bloco, mas exige que os endereços dos processos sejam relocáveis dinamicamente.

**9) (1 pt) Considerando a evolução do Gerenciamento de Processos (Aulas 04 e 09), responda:**

* **a)** O que é e para que serve o *fork()* em sistemas baseados em UNIX?
* **b)** Como as *Threads* (*Lightweight Processes*) diferem de processos tradicionais criados via *fork()* no que diz respeito ao compartilhamento da área de memória e arquivos abertos?
* **c)** O modelo *Many-to-Many* (Múltiplas threads de usuário mapeadas em múltiplas threads de kernel) resolve quais deficiências dos modelos Many-to-One e One-to-One?

**10) (1 pt) Sobre políticas de escalonamento avançadas (Aula 05), assinale a alternativa incorreta:**

* A) Em um sistema com Filas de Múltiplos Níveis, os processos são classificados de forma permanente em diferentes filas (ex: fila de processos de sistema, fila de processos interativos, fila em lote), cada uma com seu próprio algoritmo de escalonamento.
* B) As Filas de Múltiplos Níveis com Realimentação (*Multilevel Feedback Queues*) permitem que um processo mude de fila durante sua execução. Por exemplo, se um processo consome muita CPU (esgota seu quantum), ele pode ser rebaixado para uma fila de prioridade inferior.
* C) Escalonamento por Prioridades Estáticas pode gerar inanição (*starvation*), cenário onde processos de baixa prioridade nunca recebem CPU porque o sistema tem um fluxo constante de processos de alta prioridade chegando.
* D) Processos limitados por entrada e saída (*I/O-bound*) devem, estrategicamente, ser colocados nas filas de menor prioridade possível do sistema interativo, pois eles demoram muito tempo usando os discos mecânicos e atrapalhariam o uso da CPU.

[RESOLUÇÃO](resolucao/prova-11.md)

