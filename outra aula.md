
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


At = 1
Pt = 2
Zt = 5
Ct = 10

lad = "d"

tempo = 17

lanterna = true;


estados:

estado inicial:
AD = true
PD = true
ZD = true
CD = true

AE = false
PE = false
ZE = false
CE = false


estado final:
AD = false
PD = false
ZD = false
CD = false

AE = true
PE = true
ZE = true
CE = true


regras de transição:

até 2 pessoas podem passar juntos na ponte ao mesmo tempo, ao menos 1 precisa estar segurando a lanterna enquanto atravessa a ponte.
a pessoa pode ir para o outro lado da ponte e voltar se quiser quantas vezes necessario.
toda vez alguem percorre a ponte o tempo dele para atravesar sera diminuido do tempo restante.


if( per1.lad == per2.lad){
return.true

}


restrições:
para cruzar a ponte é preciso que, eles estejam juntos e ao menos um individuo atravessando esteja com a lanterna.

o tempo decorrido não pode ser maior que 17min

visitados:
Localização deles nos pontos da ponte:
AD 
PD  
ZD  
CD  

AE  
PE  
ZE  
CE  





função objetivo:
Levar as 4 pessoas para o  outro lado da ponte.






