# att_IA_15.03
1. Pesquisar  e resumir os algoritmos de busca informada


Greedy Search
Algoritmo Guloso é uma solução comum para problemas de otimização onde:
•	Realiza a escolha que parece ser a melhor no momento na esperança de que a mesma acarrete em uma solução ou prevenção de futuros problemas a nível global.
•	É simples e de fácil implementação;
•	É míope: ele toma decisões com base nas informações disponíveis na iteração corrente.
Características
•	Jamais se arrepende de uma decisão, as escolhas realizadas são definitivas;
•	Não leva em consideração as consequências de suas decisões;
•	Podem fazer cálculos repetitivos;
•	Nem sempre produz a melhor solução (depende da quantidade de informação fornecida);
•	Quanto mais informações, maior a chance de produzir uma solução melhor.

Algoritmos Gulosos vs Programação Dinâmica 
•	Em um algoritmo de programação dinâmica a escolha pode depender da solução dos subproblemas, enquanto um algoritmo guloso vai tentar escolher a melhor solução naquele momento.
•	A solução dos problemas na programação dinâmica parte de baixo para cima, enquanto um algoritmo guloso vai de cima para baixo, ou seja, na programação dinâmica, as soluções para todos os subproblemas são calculadas partindo dos menores subproblemas para os maiores.
•	Os resultados dos subproblemas na programação dinâmica são salvos, facilitando a prova de correção.
Pontos a favor
•	Simples e de fácil implementação;
•	Algoritmos de rápida execução;
•	Podem fornecer a melhor solução (estado ideal).

Pontos contra
•	Dependentes de informações;
•	Correm o risco de entrarem em loops infinitos;
•	Situacionais, só resolvem tipos específicos de problemas;
•	Decisões tomadas são irrevogáveis;



A* Search (é condição para questão 2 - entender muito bem)

Descrição do A* Search Algorithm
O algoritmo A* é um dos algoritmos mais simples de busca em grafo. Este utiliza a busca em largura como base do algoritmo. Ele garante encontrar um dos caminhos possíveis do ponto de partida até o ponto de chegada (caso este exista), no entanto, não garante que o caminho encontrado seja o melhor de todos.

O A* escolhe entre todos os caminhos possíveis de um determinado ponto, aquele que aparenta chegar mais rápido ao seu destino. Iniciando de um ponto de partida (Start), constrói-se uma árvore de caminhos iniciando deste nó, expande-se cada um deles a cada iteração, até que um dos caminhos expandidos seja o nó de chegada (Goal).
A cada iteração do seu loop principal, o A* determina qual dos caminhos deseja-se expandir primeiro. Para isso, ele seleciona aquele caminho que minimiza a função:
f′(n)=g′(n)+h′(n)
Onde g′(n) é a função de custo, que determina quão custoso é mover-se do ponto atual até este novo ponto de chegada. Um exemplo de custo seria o quão demorado é desloca-se de uma cidade para outra, ou então, o quão custoso é realizar uma jogada em um tabuleiro de xadrez (peças comidas x peças perdidas). Já a função h′(n) é a heurística do algoritmo, que dita o quão perto este caminho está do seu objetivo final (chegar ao ponto de destino). E por fim, a função f′(n) é a função prioridade que é a soma da função custo com a função de heurística.

Graph Search

Graph Search

Breadth First Search
Definição

Formalmente, uma busca em largura é um método de busca não-informada (ou desinformada) que expande e examina sistematicamente todos os vértices de um grafo direcionado ou não-direcionado. Em outras palavras, podemos dizer que o algoritmo realiza uma busca exaustiva num grafo passando por todas as arestas e vértices do grafo. Sendo assim, o algoritmo deve garantir que nenhum vértice ou aresta será visitado mais de uma vez e, para isso, utiliza uma estrutura de dados fila para garantir a ordem de chegada dos vértices. Dessa maneira, as visitas aos vértices são realizadas através da ordem de chegada na estrutura fila e um vértice que já foi marcado não pode entrar novamente a esta estrutura.
Uma analogia muito conhecida (figura ao lado) para demonstrar o funcionamento do algoritmo é pintando os vértices de branco, cinza e preto. Os vértices na cor branca ainda não foram marcados e nem enfileirados, os da cor cinza são os vértices que estão na estrutura fila e os pretos são aqueles que já tiveram todos os seus vértices vizinhos enfileirados e marcados pelo algoritmo.
Tal mecanismo permite que se descubra todos os vértices a uma distância n do vértice raiz antes de qualquer outro vértice de distância maior que n, sendo n o número de arestas para atingir qualquer outro vértice no grafo considerado. Essa característica do algoritmo permite construir uma árvore de distâncias mínimas (menor número de arestas) entre o vértice raiz e os demais, sendo que o vértice responsável por enfileirar o seu vizinho na cor branca que será o vértice pai deste na representação em árvore gerada.


Depth-First Search
Definição Formal

Representação visual de uma busca em profundidade formalmente, um algoritmo de busca em profundidade realiza uma busca não-informada que progride através da expansão do primeiro nó filho da árvore de busca, e se aprofunda cada vez mais, até que o alvo da busca seja encontrado ou até que ele se depare com um nó que não possui filhos (nó folha). Então a busca retrocede (backtrack) e começa no próximo nó. Numa implementação não-recursiva, todos os nós expandidos recentemente são adicionados a uma pilha, para realizar a exploração.
A complexidade espacial de um algoritmo de busca em profundidade é muito menor que a de um algoritmo de busca em largura. A complexidade temporal de ambos algoritmos são proporcionais ao número de vértices somados ao número de arestas dos grafos aos quais eles atravessam.
Quando ocorrem buscas em grafos muito grandes, que não podem ser armazenadas completamente na memória, a busca em profundidade não termina, em casos onde o comprimento de um caminho numa árvore de busca é infinito. O simples artifício de “ lembrar quais “nós” já foram visitados” não funciona, porque pode não haver memória suficiente. Isso pode ser resolvido estabelecendo-se um limite de aumento na profundidade da árvore.




2. Solucionar, na linguagem de sua preferência o problema 8 puzzle:

O programa deve inicializar o estado inicial do jogo (matriz 3 x 3) - pode ser um arquivo, aleatoriamente ou diretamente no código
A inicialização deve conter o valor 0 para o espaço
A interface pode ser CHUI (caracter), GUI (Graphical) ou Web
Dicas:
Leia antes https://www.cs.princeton.edu/courses/archive/fall15/cos226/assignments/8puzzle.html
Entender  Hamming priority function e  Manhattan priority function.

Pode ser feito em dupla ou individual.

A entrega deve ser feita no GIT (GitHub ou GitLab - será analisada a contribuição dos participantes para o projeto) a pergunta 1 pode estar respondida na documentação do projeto e o código deve ter licença MIT.
Você deve apresentar o seu código em sala de aula, explicando todos os pontos e decisões tomadas. Todas as referências devem ser citadas.
