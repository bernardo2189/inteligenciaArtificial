metodos de busca tecnicas de ia para motores de raciocinio
|                                                    |
Cega == sem informações == força bruta               dedutivo
|
profundidade:visitados, 
|
largura ou amplitude: visitados, fila
| completo

heuristica == com informação
 |        |
 |        dica
 |        |   |
 |        |   especialista(humano, matematica)
 |        |
 |        custos
 |            |
 |            real - g
 |            |
 |            estimado - h
 |
 subida de encosta
 |        |
 |        climb hill
 |           |
 |           profundidade
 |             |
 |             custo real
 |
 Guloso - consome menos memoria mas usa mais processador
 |   |
 |    Greedy
 |     |
 |     amplitude
 |       |
 |       custo estimado
 |
 A*
  |
  amplitude
      |
      correção do custo estimação
                        (custo real acumulado)
                                  +
                           (custo estimado)
