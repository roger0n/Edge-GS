# Sensor para o drone
## Turma: 1ESA - FIAP
## Sensor de movimento no arduino 

## integrantes
### AUGUSTO FERREIRA ROGEL DE SOUZA (RM 557709)
### MAURO CARLOS MAIA NETO (RM 556645)
#
### Componentes 
- [Arduino-uno](https://docs.wokwi.com/pt-BR/parts/wokwi-arduino-uno)
- [Biaxial-stepper](https://docs.wokwi.com/pt-BR/parts/wokwi-biaxial-stepper)
- [HC-SR04](https://docs.wokwi.com/pt-BR/parts/wokwi-hc-sr04)
- 1 Led vermelho
- 1 Breadboard
- 1 Resistor- 150 ohms
- 10 Jumpers

## Descrição do projeto - Global Solution
<p>Esse projeto consiste na criação de um sensor, que será utilizado em um drone que limpara a água dos microplásticos. O sensor servira para alertar o drone e evitar que ele bata em algo durante a sau navegação.</p>

<p><b>Ideia:</b> Utilizando o Biaxial-stepper como uma "turbina" de um drone submarino, ele giraria a todo o momento, enquanto o HC-SR04, Sensor de distância ultrassônico, mandaria os sinais e retornaria com a distancia, quando a distancia estivese menor que 60 cm, a "turbina" pararia de girar e acenderia o led vermelho, assim dando tempo do drone poder se mover para outra direção.</p>

<p><b>O codigo:</b> Para conseguirmos fazer esse projeto no arduino, utilizamos o Biaxial-stepper juntamente com sua biblioteca Stepper, definimos uma variavel const para a quantidade de passos por circulo e os pinos do motor. Agora o HC-SR04 Sensor de distância ultrassônico, definimos os pinos para o trigger e o echo e uma variavel float, chamada dist, para calcular a distancia, definimos um pino para o led tambem. No void setup, definimos a velocidade do motor, definimos o tipo do trigger e do led como OUTPUT e o tipo do echo como INPUT. No void loop, começamos com trigger desligado depois de um delay de 5 microseconds ele fica ligado e depois de um delay de 10 microseconds ele desliga denovo, assim o trigger fica lançando um pulso sonico o tempo inteiro para o echo receber, utilizando a variavel dist com o comando pulseIn nos conseguimos o valor que o echo armazena do trigger, depois temos que converter esse valor para cemtimetros dividindo por 58 assim obtendo a distancia em cemtimetros, agora usando condições, se a distancia for maior que 60 o motor começa girar e led fica desligado, se não for maior que 60 o motor para e o led acende.</p>

<p><b>Conclusão:</b> Este projeto, ajudara o drone a se locomover sem prejudicar nenhum animal ou se danificar durante o processo de limpeza das águas.</p>