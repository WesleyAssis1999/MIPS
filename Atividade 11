.data
pedirnomes: .asciiz "Informe o nome dos times: "
pedirplacar: .asciiz "Informe o placar: "
empate: .asciiz "Empate"
placarx: .asciiz " x "
time1: .space 20
time2: .space 20




.text
li $v0, 4
la $a0, pedirnomes
syscall      # mensagem de entrada de nomes

li $v0, 8
la $a0, time1
li $a1, 20
syscall      # Entrar com o nome do time1:

la $a0, time2
syscall      # Entrar com o nome do time2:



#--------entrada com o placar
li $v0,4
la,$a0,pedirplacar
syscall  #mensagem pedindo o placar

li $v0, 5
syscall 
move $t0, $v0     #Placar time 1

li $v0, 5
syscall
move $t1, $v0     #Placar time 2

bgt $t0, $t1, time1venceu
bgt $t1,$t0, time2venceu

#Aqui aconteceu um empate
li $v0, 4
la $a0, empate
syscall 

j saida #Encerrar o programa

time1venceu: 
li $v0,4
la $a0, time1
syscall
j saida

time2venceu:
li $v0,4
la $a0, time2
syscall


saida:
li $v0,1
move $a0, $t0
syscall

li $v0,4
la $a0,placarx
syscall 

li $v0,1
move $a0, $t1
syscall

