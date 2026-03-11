
Problema da travessia da ponte

Há 4 pessoas: cientista, zelador, professora e aluno. Que precisam passar pela ponte.

Cada um tem um tempo de travessia:

aluno: leva 1 minuto para cruzar a ponte
professora: leva 2 minutos
zelador: 5 minutos
cientista: 10 minutos

O problema é: qual a sequência de travessia para que o tempo total seja no máximo de 17 minutos.

Contudo, para cruzar a ponte é preciso usar uma lanterna e no máximo duas pessoas podem cruzar a ponte. Qualquer pessoa cruzando a ponte precisa segurar a lanterna.

Trabalho avaliado é a modelagem:
	1) Estados
	2) Regras de Transição
	3) Restrições
	4) Visitados
	5) Função objetivo
///////////////////////////////////////////////////////

A
P
Z
C


A.t = 1
P.t = 2
Z.t = 5
C.t = 10

lad = "d" ou "e"

tempo = 17

lanterna = true;"variavel interna dos A, P, Z, C, para saber quem tem a lanterna"


estados:

estado inicial:
A.lad = "e"
P.lad  = "e"
Z.lad  = "e"
C.lad  = "e"
Ped == 4
Pel == 0

estado final:
A.lad = "d"
P.lad = "d"
Z.lad = "d"
C.lad = "d"
Ped == 0
Pel == 4


regras de transição:

até 2 pessoas podem passar juntos na ponte ao mesmo tempo, ao menos 1 precisa estar segurando a lanterna enquanto atravessa a ponte.
a pessoa pode ir para o outro lado da ponte e voltar se quiser quantas vezes necessario.
toda vez alguem percorre a ponte o tempo dele para atravesar sera diminuido do tempo restante.

if(dois_ao_mesmo_tempo){
	if(per1.lad == per2.lad){

		if(per1.lanterna == true or per2.lanterna == true){ 
		  if(per1.t > per2.t){
		    tempo -= per1.t 
		  	}else{
			tempo -= per2.t 
		  	}
		return.true
		}else{
        return.false
		}

   }else{
    return.false
   }
}else{

if(per1.lanterna){
return.true
}


}



restrições:
para cruzar a ponte é preciso que, estejam juntos e ao menos um individuo atravessando esteja com a lanterna.
no caso de apenas um atravessar é necessario estar com a lanterna

o tempo decorrido não pode ser maior que 17min

visitados:
Localização deles nos pontos da ponte:

lad = posição de cada individuo.
peD = quantia de pessoas no lado direito
Pel= quantia de pessoas no lado esquerdo 





função objetivo:
Levar as 4 pessoas para o  outro lado da ponte.






