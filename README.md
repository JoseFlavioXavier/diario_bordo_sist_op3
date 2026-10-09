# diario_bordo_sist_op3!

UNICESUMAR LONDRINA

DISCIPLINA:Sistemas Opercaionais

Docente: Leonardo Rocha

Titulo: Thread vs Processo, uma explicação conceitual.

Discente: José Flávio Xavier RA: 25357647-2

Londrina-PR

1-Sintese teórica

A)Thread Vs Processo.
Um Thread é menor unidade de processamento, mas podemos perguntar, "Menor unidade de processamento de que?". Essa pergunta é respondida explicando o que é um processo.
O processo é um conjunto de instruções, dados e status. E para responder a pergunta "O thread é  a menor unidade de processamento de que?". Quando uma aplicação é criada e vai para memória, se transforma em um processo. O processo precisa de pelo menos um Thread, então, ele é um subconjunto, ou menor unidade de processamento do próprio processo.

B)A questão de velocidade.
Apesar de dividirem o mesmo local na memória, o processo necessita de contexto para sua criação e execução, o conjunto de instruções, dado e status, sendo assim, ele consume mais memória para. O thread, por se tratar de uma unidade mais elementar, necessita de menos recursos computacionais. Quando são colocados em uma escala de cem mil usuários, acaba sendo mais rápido a criação de threads.

C)Thread nos modo usuário e modo kernel
O thread no modo usuário é executado e gerenciado de mamenira independe do modo kernel, ou seja, quem é faz o gerenciamento dos thereads pela própria aplicação em questão e o núcleo não possui o conhecimento dos threads.Cada aplicação tem suas tabelas de theread. O thread em modo kernel é executado e gerenciado pelo próprio kernel. O núcleo faz o gerenciamento, podendo bloquear as threads guargando as informações de contextos, e passando a prioridade de execução para outro thread.

2-Diagnóstico do Problema

A)Usuário A VS Usuário B
Ao clicar no extato momemnto em comprar o que irá acontecer é, será verificado a disponibilidade do assento A15, para ambos os usários ao mesmo tempo, e como ela estará disponível para o usário A e o usário B, ambos conseguiram comprar o assento A15 e o sistema irá processar a comprar normalmente.

B)A condição de corrida
A condição de corrida é quando dois ou mais thereads tentam acessar os mesmo métodos computacionais ao mesmo tempo, criando uma condição de duplicidade.

A Solução Arquitetural

A)A solução para o nosso problema
A solução para o nosso problema reside em dois principais conceitos, região crítica e exclusão mútua. O primeiro conceito, região crítica, as aplicações compartilham de um mesmo segmento de código. Esse segmento contém uma região crítica que determina que apenas uma aplicação irá continuar, "Mas quem protege essa região especifica". Para explicar isso, vamos utlizar o segundo conceito, a exclusão mútua, ela quem protege essa região específica. A função lock, que traduzindo para o portugûes é fechadura/cadeado, funciona com uma fechadura da região crítica. o Mutex, é um tipo de lock mais específica. O mutex, determina que o primeiro processo que teve acesso a região crítica será "trancado" e somente o esse mesmo processo poderá destrancar. Aplicando ao nosso progeto, isso impede que ocorra compra de assentos duplicados, evitando confussões e possíveis problemas juridicos.


Referencias bibliográficas:
CÓDIGO FONTE TV. Thread (entenda como sua aplicação funciona). Direção de Gabriel Froes e Vanessa Weber. [S. l.]: YouTube, 14 set. 2020. 1 vídeo (11 min 56 s). Publicado pelo canal Código Fonte TV. Disponível em: https://www.youtube.com/watch?v=xNBMNKjpJzM. Acesso em: 8 out. 2026.

GEEKSFORGEEKS. Race Conditions. [S. l.]: GeeksforGeeks, [2026?]. Disponível em: https://www.geeksforgeeks.org/java/race-conditions/. Acesso em: 8 out. 2026.

IBM. Understanding threads and processes. [S. l.]: IBM, [2026?]. Disponível em: https://www.ibm.com/docs/pt-br/aix/7.3.0?topic=programming-understanding-threads-processes. Acesso em: 8 out. 2026.

ISMAEL. C++ Intro OS Kernel. [S. l.]: PUC-Rio, [20–?]. 1 apresentação de slides (notas de aula). Disponível em: https://web.tecgraf.puc-rio.br/~ismael/Cursos/YC++/aulas/Basic/ModuloI/C++_Intro_OS_Kernel.pdf. Acesso em: 8 out. 2026.

JIANG, Fontaine. Critical Section. [S. l.]: Fontaine Jiang's Blog, 17 out. 2017. Disponível em: https://fontainejiang.wordpress.com/2017/10/17/critical-section/. Acesso em: 8 out. 2026.

ORACLE. Processes and Threads. [S. l.]: Oracle, [2026?]. (The Java™ Tutorials). Disponível em: https://docs.oracle.com/javase/tutorial/essential/concurrency/procthread.html. Acesso em: 8 out. 2026.

[SOBRENOME, Nome] (Autor do artigo da Revista Campo Digital). [Título do artigo]. Campo Digital, [S. l.], v. [X], n. [X], p. [XX–XX], [Ano]. Disponível em: https://revista2.grupointegrado.br/revista/index.php/campodigital/article/view/311/145. Acesso em: 8 out. 2026. (Lembre-se de substituir os campos entre colchetes com os dados reais do artigo).