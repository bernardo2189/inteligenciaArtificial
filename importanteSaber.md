# Aula 1

Professor falou sobre:
    - Base de conhecimento
    - Raciocínio automatizado

    - Aprendizado de máquina

#Aula 2

//ordem em que serão ensinadas...
Sistemas de comportamento Inteligente
 -base de conhecimento
   -Armazenamento de experiencia (PROLOGO)
 -motor de raciocinio / raciocinio automatizado (dedução e indução)
   -metodos de busca e SMA 
      -cegos: amplitude e profundidade
      -heuristicos: subida de encosta, guloso, A*, Algoritimos Geneticos
 -aprendizado de maquina - reconhecer padrões por repetição
      -redes neurais
///

 -Metodos de Busca
  -modelagem do problema / solução
      1) estados (inicial/construtor, intermediarios/construtor2, final)
      2) Regras de transição -> métodos que modificam o objeto
      3) Restrição (estado que não pode ser gerado)
      4) visitas (lista ou uma arvore ou um hashmap)
      5) fução objetivo

A) problemas da torres de hannoi
Estado 
     //toda pilha tem os seguintes comandos:empty, peek, psuh/add, pop/remove
     Pilha t1 = new stack();
     Pilha t2 = new stack();
     Pilha t3 = new stack();

Estado Inicial
     t1.push(3)
     t1.push(2)
     t1.push(3)

Estado Final ou função Objetivo/Meta
     t1.empty() && t2.empty()


Regras de Transição
    r1 - mover t1 para t2
    if(ehvalido(t1,t2)){
     public void movert1_t2(){
     t2.push(t1.pop()); 
    } 
      Estado novo = new Estado(t1,t2,t3,"movendo topo 1 para topo t2")

      if(!visitados.contains(novo)){
          visitados.add(novo);
      }
    }
    r2 - mover t1 para t3
     public void movert1_t3(){
     t3.push(t1.pop()); 
    }
    r3 - mover t2 para t1
     public void movert2_t1(){
     t1.push(t2.pop()); 
    }
    r4 - mover t2 para t3
     public void movert2_t3(){
     t3.push(t2.pop()); 
    }
    r5 - mover t3 para t1
     public void movert3_t1(){
     t1.push(t3.pop()); 
    }
    r6 - mover t3 para t2
     public void movert3_t2(){
     t2.push(t3.pop()); 
    }

//Restrições
    public boolean ehvalido(Stack Origem, Stack Destino){
            if(origem.empty()){
                  return false;
            }
            if((int)Origem.peek() > (int)Destino.peek()){
            return true;
            }
    }

//Visitados - lista ou arvore ou hashmap


["[321][][]","[32][][]"]
