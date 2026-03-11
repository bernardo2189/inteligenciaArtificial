
Maze Runner labirinto


matriz[n,n] char*

1 definir obstaculos em celulas de maneira aleatoria
% definida pelo->

2 sortear a posição linha, coluna E
3 sortear a posição linha, coluna S

problema/objetiva

descobrir um caminho entre E e S
relatar os comandos


estados--------------------------------

estados contendo = matriz de [n,n] --> char
 'E' - entrada
 's' - saida
 '@' - obstaculo
-linha entrada - int
-coluna entrada - int
-linha da saida - int
-coluna da saida - int

Estado inicial: 'E' sorteado em linha e coluna
                'S'    ||    ||    ||      ||
                '@' sorteadoS em linhaS e colunaS

Estado Final: 'E' na mesma celula que 'S'

REGRAS DE TRANSIÇÃO

cima: linhaentrada--
baixo: linhaentrada++
esquerda: colunaentrada--
direita: colunaentrada++


restrições

linhadeentrada == n-1
linhaentrada == n==0


visitados
so precisa salvar o "movimento" da linha e coluna do 'E'


funções objetivo

linha entrada == linha da saida
              &&
coluna entrada == coluna da saida

MISSIONARIOS E CANIBAIS
Há 3 missionários e 3 canibais. Há também um barco que vai da margem esquerda para a margem direita e vice-versa, sempre levando um ou duas pessoas. Todas as pessoas estão na margem esquerda e precisam ir para a margem direita. Porém, há restrições: em momento algum pode ficar mais canibais do que missionários em uma das margens.

ME = 0-3
CE = 0-3
MD = 0-3
CD = 0-3

estado incial

ME = 3
CE = 3
MD = 0
CD = 0

Estagio final
              ME = 0
              CE = 0
              MD = 3
              CD = 3

Restrições

if(CE> ME)
return false
if(CD > MD)
return false
if(CE < ME)
return false
if(CD < MD)
return false

regras de transição
barco apenas pode ir para o outro lado do rio*
O barco sempre sai de um lado do rio carregando ao menos 1 individuo*

Capacidade do barco: 1-2

barco se Move.


problema/objetivo

Levar os 3 missionarios e 3 canibais para o outro lado do rio.
relatar os comandos

