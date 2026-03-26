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
//////////////////////////////////////////////////////////////////
fato
   |
   sentença ou predicados ou assertiva

   papel(alex, professor)
   papel(marzari, aluno)
   papel(gustavo, aluno)
   papel(gustavo, monitor)
   estado(luz, ligado)
   estado(ar-condicionado, desligado)
   matriculado(dereis, jogos, ia)
   matriculado(dereis, jogos, design)
   progenitor(jura, alex)
   progenitor(jura, tina)
   

   prolog
      |
      argumentos ou parametros
       |  |  |
       |  |  objeto
       |  |    |
       |  |    minusculo
       |  |
       |  literal
       |     |
       |     "Matheus dos reis"
       |
       variavel
          |                    teste(Alex, alex)                              
          |                            |      |
          letra maiuscula          variavel  objeto
                 |
                 1 letra
/////////////////////////////////////


%base.pl
%fatos
      %sentencas ou predicados ou assinaturas de funcoes 




jogo("CS", "Counter Strike", 16, "FPS").
jogo("LOL", "league of Legends", 18, "MOBA").
jogo("AID", "Alone in the Dark",16, "SU").
jogo("GTA", "Grand Thief Auto",18, "SB").
jogo("MC", "Minecraft",0, "SB").

tipo("SB", "Sandbox").
tipo("FPS", "First Person Shooter").
tipo("MOBA", "Multiplayer Online Battle Arena").
tipo("SU", "Survivel").


%regras
       %sentencas com variaveis acompanhadas por :-

indicacaolivre(NomeJogo) :-
    jogo(_,NomeJogo,Idade,_),
    Idade == 0.
    


progenitor(hebert, cleber).
progenitor(hebert, homer).
progenitor(homer, bart).
progenitor(homer, lisa).
progenitor(homer, meg).
progenitor(marge, bart).
progenitor(marge, lisa).
progenitor(marge, meg).
progenitor(bart, alex).
progenitor(bart, tina).


avo(A,N) :-
    progenitor(A,P),
    progenitor(P,N).


irmaos(A,B) :- progenitor(P,A),
               progenitor(P,B),
               A \= B.
    
tio(T,S) :-
     irmaos(I,T),
     progenitor(I,S).

cunhados(A,B) :-
