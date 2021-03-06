<h1 align="center">
  <img src="images/header-animation.gif">
</h1>

---

<!-- 
[![Linkedin Badge](https://img.shields.io/badge/-Mateus%20Antonio-0282d0?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/mateus-antonio-robotica/)](https://www.linkedin.com/in/mateus-antonio-robotica/)

[![Instagram Badge](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](instagram.com/bittoin_)
[![Youtube Badge](  https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/channel/UCnkVhwxeXeJvUZx6BJ5Wa2Q)
[![Twitch Badge](https://img.shields.io/badge/Twitch-9146FF?style=for-the-badge&logo=twitch&logoColor=white)](twitch.tv/bittoin)
[![Telegram Badge](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](t.me/bittoin)
-->

<a href="https://instagram.com/bittoin_">
<img border="0" alt="Instagram" src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white">
</a>

<a href="https://www.youtube.com/channel/UCnkVhwxeXeJvUZx6BJ5Wa2Q">
<img border="0" alt="Youtube" src="https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white">
</a>

<a href="https://www.twitch.tv/bittoin">
<img border="0" alt="Twitch" src="https://img.shields.io/badge/Twitch-9146FF?style=for-the-badge&logo=twitch&logoColor=white">
</a>

<a href="https://t.me/bittoin">
<img border="0" alt="Telegram" src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white">
</a>

<h3 align="center">
  Uso de linguagens de programação para uma maior diversidade de projetos.
</h3>

## Índice

+ [Sobre](#sobre)
  + [Circuito](#circuito)
  + [Interface Gráfica](#interface-grafica)
  + [Placa de Circuito Impresso (PCB)](#pcb)
+ [Primeiros Passos](#comecando)
  + [Pré-requisitos](#pre_req)
  + [Instalação](#instalacao)
+ [Uso](#uso)
+ [Código](#codigo)
  + [Código Arduino](#codigo-arduino)
  + [Código Qt](#codigo-qt)
+ [Melhorias](#todo)

<h2 id="sobre">Sobre</h2>

Hoje projetos de hardware não sobrevivem mais apenas com hardware, pois a tendência é sempre ter cada vez mais tecnologias e dispositivos conectados. Cada vez mais temos opções de softwares que integram dispositivos, fornecem dados e interagem com o usuário de maneira simples e intuitiva. Além disso, sabemos que projetos com Arduino e componentes eletrônicos são capazes de realizar inúmeras tarefas e serem utilizados em diversas soluções tecnológicas para problemas do dia a dia. Unindo isso ao poder do software, é possível potencializar a capacidade dos projetos e tirar mais ideias do papel, criando cada vez mais soluções e atingindo públicos diferentes.

O objetivo do projeto foi desenvolver uma interface gráfica para o controle e leitura de dados de alguns dispositivos conectados ao Arduino, a fim de comprovar a capcidade e validar conceitos de programação para a construção de um Software integrado com hardware.

O framework utilizado para o projeto foi o Qt, uma toolkit em C++ multiplataforma, ou seja, o software criado para este projeto funciona no Windows, Linnux e MacOS.

Abaixo você pode visualizar o circuito montado no simulador [Tinkercad](https://www.tinkercad.com/). Visto que o circuito validado é físico e integrado com um software que roda em um Sistema Operacional, a simulação não servirá para demonstrações, apenas para referência na visualização do circuito.

<div align='center'>
    <img src="images/circuit.png">
    <p>Figura 1. Representação do Circuito montado no Tinkercad</p>
</div>

<h3 id="circuito">Circuito</h3>

<div align='center'>
    <img src="images/esquematico-pcb.png">
    <p>Figura 2. Esquemático do Circuito</p>
</div>

O circuito possui alguns componentes que juntos são capazes de provar vários conceitos na montagem de circuitos e programação para Arduino. O potênciometro funciona como um dispositivo que substitui a leitura de qualquer tipo de sensor, enquanto o led atua para validar dispositivos que ligam e desligam, além de testes com o PWM. Por último, o Servo Motor como um atuador, para se movimentar e atuar conforme a necessidade.

<h4 id="materiais">Lista de Materiais</h4>

+ Arduino Uno R3
+ Protoboard
+ Fios macho-macho
+ Led difuso 5mm
+ Potênciometro 10k Linear
+ Micro Servo Motor
+ Resistor 220Ω
+ Resistor 10kΩ

<h3 id="interface-grafica">Interface Gráfica</h3>

A interface gráfica, como pode ser vista na figura abaixo, é simples e possui algumas funcionalidades. Possui uma área de reconhecimento de portas, para identificar as placas que estão conectadas e um botão para atualizar a lista. Possui também um botão para conectar e um label para indicar se está conectado ou desconectado.

Abaixo, na área de controle, tem um slider responsável por alterar a luminosidade do LED e a própria imagem do LED é um botão, para ligá-lo e desligá-lo quando for clicado. Na direita tem um slider semelhante, para controlar o Micro Servo Motor de 0º a 180º, além de poder controlá-lo também pelo teclado.

Por último, na interface podemos ver um display de leitura do potênciometro, que mostra o valor inteiro ou em valor percentual, indicando o início e o fim do seu curso. Esse potênciometro poderia ser substituído por qualquer tipo de sensor que gere dados.

<div align='center'>
    <img src="images/tela-app.png">
    <p>Figura 3. Interface simples de controle e leitura feita em Qt</p>
</div>

<h3 id="pcb">Placa de Circuito Impresso (PCB)</h3>

Para que o projeto não fosse apenas um circuito montado em uma protoboard, uma PCB foi pensada para futuramente ser utilizado como um protótipo fácil de utilizar em um minicurso ou workshop. Para isso, o mesmo circuito testado e validado foi idealizado para se tornar um Shield para Arduino.

Um shield consiste em uma placa criada com um propósito específico que é encaixada em cima de uma placa Arduino com todas as conexões já feitas, deixando a experiência mais fácil, direta, estilo plug-and-play.

<div align='center'>
    <img src="images/pcb.png">
    <p>Figura 4. Esquemático da PCB</p>
</div>

No gif abaixo é possível observar os pinos laterais, que seriam encaixados diretamente na placa Arduino, enquanto no centro da placa se encontram todos os componentes e slots para encaixar os componentes do projeto.

<div align='center'>
    <img src="images/demo-pcb.gif">
    <p>Figura 5. Modelo 3D da PCB</p>
</div>

> Software utilizado para a criação da PCB: *EasyEDA*

<h2 id="comecando">Começando</h2>

Siga estas instruções para criar, replicar e modificar o modelo do projeto na sua máquina. 

<h3 id='pre_req'>Pré-requisitos</h3>

Os softwares utilizados para a criação e execução do código.

> Qt: Kit Desktop 5.15.2
> Arduino: Arduino IDE 1.8.13 ou PlatformIO

<h3 id='instalacao'>Instalação</h3>

Para executar o código Qt, basta clonar este repositório ou fazer o download. Depois abrir a IDE do Qt (Qt Creator), **File > Open file or project** e depois selecionar o arquivo **arduino-gui.pro** dentro da pasta do projeto **arduino-gui**.

O código do Arduino pode ser encontrado na pasta *codes/qt_arduino.ino*. Para utilizá-lo, basta ter a IDE do Arduino instalada e realizar o upload do código na placa. Além disso, ter todos os componentes conectados de acordo com o circuito esquemático mostrado na primeira figura.

<h2 id="uso">Uso</h2>

<div align='center'>
    <img src="images/demo-interface-compressed-min.gif">
    <p>Figura 6. Exemplo de uso da Interface feito durante a live de desenvolvimento</p>
</div>

<!--

<h2 id="codigo">Código</h2>

<h3 id='codigo-arduino'>Código Arduino</h3>

<h3 id='codigo-qt'>Código Qt</h3>

-->

<h2 id='todo'>Features</h2>

+ [x] Controla luminosidade do LED pela interface
+ [x] Liga e desliga LED pelo teclado
+ [x] Controla posição do Servo Motor pela interface
+ [x] Controla posição do Servo Motor pelo teclado
+ [x] Visualiza valor do potenciômetro/sensor em um display
+ [x] Visualiza o valor do potenciômetro/sensor em valor percentual
+ [x] Painel de verificação de placas conectadas no computador
+ [x] Botão de conexão

Alguns outros componentes básicos como push-button e sensor LDR seriam uma ótima adição ao projeto, porém o potênciometro já serve como substituto para a maioria dos possíveis inputs que poderíamos ter.

Algumas melhorias que poderiam ser feitas futuramente:

+ Botão de conectar vira desconectar
+ Maior responsividade entre os componentes e imagens
+ Melhoria no design da interface (UI/UX)
+ Controle de mais componentes

## Licença

Copyright © 2021 [Mateus Antonio da Silva](https://github.com/bittoin).<br />
This project is [MIT](https://github.com/bittoin/Qt-GUI-for-Arduino/blob/main/LICENSE) licensed.