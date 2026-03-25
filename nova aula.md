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
 A*(A estrela)
  |
  amplitude
      |
      correção do custo estimação
                        (custo real acumulado)
                                  +
                           (custo estimado)


////////////////////////// outra aula ///////////////////////////

revisão
metodos de busca (soluções)
 |                    |
 |                    chegar em estado desejado final(seu aproximado)
 |                    |
 |                    conjunto de passos até estado desejado
 |                                                                                                                   peofundidade(motor de raolog)
 |                                                                                                                   |
 |                                                                                              ----> cegos ou força |--largura/amplitude
 ->  tipos de problemas                                                                         |                               |
 |          |                                                                                                                   -->fila
 |          -diagnosticos == reconhecer padrões                                                 |
 |                        |
 |                        trinamento = repetição
 |          -> não se sabe os passos ate o estagio final
 |                                                                                              |
 |
 1->  base de conhecimento                                                                      
 2-> motores de raciocinio----------------------------------------------------------------------|
 3->aprendizado       |
    de maquina        ->dedução -> metodo de força bruta profundidade
         |                                                                                      |                     custos: Real ou/e Calculados
         ->reconhecer padrões por amostra/treinamento supervisionado ou não supervisionado                              |
                                                                                                                                                     Subidas de encostas
                                                                                                |                       |                            |             ->profundidade(g(n))
                                                                                                ---->heuristicos ou informados-----------------------|-Gulosos->largura(h(n))
                                                                                                                                                     |
                                                                                                                                                     |
                                                                                                                                                     |
                                                                                                                                                    A*(a estrela) g(n) + h(n)
           
