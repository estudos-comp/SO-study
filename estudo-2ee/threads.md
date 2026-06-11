# Threads

Um processo tradicional, também chamado de processo "pesado", possui apenas um único fluxo de controle, o que significa que ele executa apenas uma tarefa por vez. Já uma Thread (ou processo leve) é a unidade básica de uso da CPU que permite a um único programa ter múltiplos fluxos de controle rodando ao mesmo tempo.

Na organização da memória, cada thread possui o seu próprio ID, um contador de programa, um conjunto de registradores e uma pilha particular. O grande diferencial, no entanto, é o compartilhamento: todas as threads que pertencem a um mesmo processo dividem a mesma área de código, de dados e os recursos do sistema operacional (como arquivos abertos e sinais).

É essa estrutura estrutural que permite, por exemplo, que um processador de textos use uma thread para ler o que você digita, enquanto outra thread faz a verificação ortográfica em segundo plano, tudo rodando dentro do mesmo processo

## Vantagens

As quatro grandes vantagens práticas de se adotar a arquitetura de threads são:

1. Responsividade: O programa continua respondendo ao usuário mesmo se uma parte dele estiver bloqueada ou executando uma tarefa demorada. Um exemplo clássico é um navegador web que permite a você clicar em botões enquanto uma imagem pesada ainda está sendo carregada em outra thread.
2. Compartilhamento de recursos: Por padrão, todas as threads de um mesmo processo dividem a mesma memória e o mesmo código, permitindo que várias atividades ocorram no mesmo espaço de endereçamento sem precisarem de técnicas complexas de comunicação.
3. Economia: Como as threads já nascem compartilhando os recursos do processo pai, criar uma nova thread ou alternar a execução entre elas exige muito menos memória e esforço do sistema operacional do que criar um processo inteiro do zero.
4. Utilização de arquiteturas multiprocessadas: Em computadores com vários processadores (ou múltiplos núcleos), as threads podem ser distribuídas para rodarem de forma genuinamente paralela, cada uma em uma CPU diferente, multiplicando o desempenho da aplicação

## Threads em Java

Em Java, o suporte a threads já vem embutido na própria linguagem, e todo programa roda pelo menos uma thread principal (o método main).
Para criar threads adicionais, você tem duas opções práticas:

1. Estender a classe Thread: Você cria uma classe que herda diretamente as propriedades de thread.
2. Implementar a interface Runnable: Essa é a alternativa mais flexível. Como o Java não permite herança múltipla, se a sua classe já herdar de outra, ela não pode estender Thread ao mesmo tempo. Nesses casos, você é obrigado a usar a interface Runnable.

Em ambos os casos, a lógica de execução é a mesma: apenas criar o objeto no código não inicia a tarefa. Você precisa obrigatoriamente chamar o método start(). É ele quem pede para a Máquina Virtual Java (JVM) alocar memória e acionar o método run(), que é onde o seu código real fica.
Por fim, durante esse ciclo, a thread trafega por quatro estados básicos:

- Novo: O objeto foi criado, mas o start() ainda não foi chamado.
- Executável: A thread está pronta e rodando na JVM.
- Bloqueado: A thread pausou porque pediu uma operação de E/S (como ler um arquivo) ou recebeu um comando como sleep().
- Morto (Terminado): O código do método run() chegou ao fim.
