# movel
implementação em Javasxript da difusão atômica atraves do metodo do sequenciador movel, onde as regras deste metodo são: 
* Para tolerar a falta do sequenciador fixo é proposta então, a
abordagem do sequenciador móvel.
* Nesta abordagem é definido um grupo de processos
sequenciadores, formando um anel lógico, que recebe todas as
mensagens do grupo emissor.
* Apenas um processo sequenciador, possuidor do bastão, tem o
privilégio de repassar as mensagens ao grupo receptor, em uma
ordem especifica.
* Como cada processo receptor conhece a ordem de sequenciadores
no anel lógico, os receptores do grupo conseguem estabelecer
uma ordem total.
* Quando um emissor deseja enviar uma mensagem ao grupo
receptor, ele difunde a mensagem no grupo sequenciador. O
sequenciador que possuir o privilégio (token) repassa a mensagem
aos receptores.
* O grupo sequenciador não precisa ter muitos membros (2 a 4
membros).
67
* Esta abordagem resolve o problema dos dois algoritmos
anteriores: o grupo emissor poder ser escalável e não há um
simples ponto de falha.
* Problemas dessa abordagem:
− Perda do token: processo que está usando o token falha;
− O grupo receptor tem que saber a sequência do anel lógico dos
sequenciadores.
