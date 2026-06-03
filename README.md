# Maquina_Enigma
<img width="300" height="234" alt="enigma-300x234" src="https://github.com/user-attachments/assets/ac9ac5d2-1233-403e-a524-6e0a65171210" />


Máquina Enigma usada pelos nazistas

## 💻 Sobre o projeto
Esse projeto consiste em desenvolver uma maquina enigma por meios de simulação digital


## 🎯 Visão Geral
O enigma possui as seguintes etapas principais: 
**Entrada de dados -> Distribuidor -> Criptografia/Decriptografia -> Saida de dados**

<img width="896" height="692" alt="main" src="https://github.com/user-attachments/assets/6b00f6a7-c782-49cd-a707-bbe1219b9b86" />



## 🔍 Explicação dos blocos
>**Entrada de dados:** Foi utilizado o teclado para permitir digitar textos e números
>
><img width="248" height="83" alt="teclado" src="https://github.com/user-attachments/assets/3640ae3a-007f-42f0-a699-de1c8531d17e" />

´´´

>**Distribuidor:** Recebe a letra digitada pelo teclado e verifica se o que foi digitado é uma letra, pois o nosso projeto só criptografa/decriptografa letras, encaminhando o que foi digitado para seu devido destino
>
><img width="321" height="143" alt="Distribuidor" src="https://github.com/user-attachments/assets/1c213578-1256-4b6c-8c13-9fa4a6704138" />

´´´

>**Criptografia:** Recebe a letra digitada pelo teclado e ao passar por um conjunto de rotores, refletor e plugboard, envia para a saida a letra criptografada
>
><img width="848" height="206" alt="Criptografia" src="https://github.com/user-attachments/assets/84d8717f-8e25-49f2-9920-df0ca6210e2a" />

´´´

>**Decriptografia:** Recebe a letra digitada pelo teclado e ao passar por um conjunto de rotores, refletor e plugboard, envia para a saida a letra decriptografada
>
><img width="852" height="194" alt="Decriptografia" src="https://github.com/user-attachments/assets/48c6d847-87ee-40a9-b740-a4205b12b749" />

´´´

>**Saída de dados:** Depois de processados, os dados são exibidos no TTY que é um componente do Logisim que simula uma tela
>
><img width="303" height="202" alt="TTY" src="https://github.com/user-attachments/assets/c566260e-2729-4867-b548-bc494c1ab53c" />



## 🛠 Analisando cada componente...
>**Verificador:** Ele é responsável por verificar se o que foi digitado é uma letra ou não, para isso ele verifica se o que foi digitado está dentro do intervalo dos valores hexadecimais das letras pela tabela ASCII
>
><img width="316" height="134" alt="Verificador" src="https://github.com/user-attachments/assets/c40243f1-9819-4011-a6fd-d74930e8fd2b" />

´´´

>**PlugBoard:** Ele realiza trocas de pares de letras antes e depois da passagem pelos rotores e refletor
>
><img width="458" height="118" alt="PlugBoard" src="https://github.com/user-attachments/assets/99f7239a-1b2c-4452-89b4-7b811b59805e" />

´´´

>**Controller:** Ele é responsavel por simular, junto com o contador, a rotação dos rotores bem como permitir que os valores não ultrapassem os valores haxadecimais das letras, mantendo o sistema dentro do intervalo de letras.
>
><img width="556" height="167" alt="Controller" src="https://github.com/user-attachments/assets/0aea2109-49ab-4de4-837c-959200dd744d" />

´´´

>**Controller Inverso:** Ele é responsavel por simular a rotação no sentido inverso, usado no bloco da decriptografia 
>
><img width="542" height="157" alt="Controller Inverso" src="https://github.com/user-attachments/assets/5c26f8b7-dd55-4080-be69-9d8dee494310" />

´´´

>**Rotor 2:** Ele simula o rotor fisico, possuindo uma cifra especifica
>
><img width="451" height="121" alt="R2" src="https://github.com/user-attachments/assets/2adaee46-f91a-491e-8254-1f2a6aac8a0e" />

´´´

>**Rotor 2 Inverso:** Ele funciona igual ao Rotor 2 porém possue a cifra inversa
>
><img width="465" height="120" alt="R2!" src="https://github.com/user-attachments/assets/d6ce4b7f-bfaa-4020-9fc5-f21fa461251f" />

´´´

>**Rotor 1:** Ele simula o rotor fisico, possuindo uma cifra especifica
>
><img width="456" height="119" alt="R1" src="https://github.com/user-attachments/assets/dbc8a6ff-e581-458e-91b9-c3ca4c7798f2" />

´´´

>**Rotor 1 Inverso:** Ele funciona igual ao Rotor 1 porém possue a cifra inversa
>
><img width="471" height="120" alt="R1!" src="https://github.com/user-attachments/assets/a72f9795-2e70-41b8-93a7-45fd86dced19" />

´´´

>**Refletor:** É o componente fixo que inverte o sentido e acaba devolvendo o sinal aos rotores.
>
><img width="451" height="121" alt="Refletor" src="https://github.com/user-attachments/assets/2cf278fe-9d3d-4308-a8da-dc22ca49fb37" />



## 📖 Cifras
Abaixo estão as cifras usadas:

|Posição|Letra| | Cifra A |	A Inversa | | Cifra B | B Inversa |  | Plugboard | Refletor |
| :---: | :---: |:---:| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| `00001` | **a** |   | g | n |   | i | n |   | f | t |
| `00010` | **b** |   | d | y |   | u | p |   | t | h |
| `00011` | **c** |   | y | z |   | r | h |   | m | i |
| `00100` | **d** |   | u | b |   | x | j |   | g | g |
| `00101` | **e** |   | n | i |   | p | l |   | z | f |
| `00110` | **f** |   | q | q |   | s | t |   | a | e |
| `00111` | **g** |   | m | a |   | k | s |   | d | d |
| `01000` | **h** |   | o | r |   | c | q |   | p | b |
| `01001` | **i** |   | e | t |   | z | a |   | o | c |
| `01010` | **j** |   | r | u |   | d | k |   | k | w |
| `01011` | **k** |   | p | m |   | j | g |   | j | s |
| `01100` | **l** |   | v | w |   | e | u |   | w | q |
| `01101` | **m** |   | k | g |   | n | o |   | c | x |
| `01110` | **n** |   | a | e |   | a | m |   | s | v |
| `01111` | **o** |   | s | h |   | m | w |   | i | z |
| `10000` | **p** |   | w | k |   | b | e |   | h | y |
| `10001` | **q** |   | f | f |   | h | v |   | x | l |
| `10010` | **r** |   | h | j |   | t | c |   | y | u |
| `10011` | **s** |   | z | o |   | g | f |   | n | k |
| `10100` | **t** |   | i | x |   | f | r |   | b | a |
| `10101` | **u** |   | j | d |   | l | b |   | v | r |
| `10110` | **v** |   | x | l |   | q | z |   | u | n |
| `10111` | **w** |   | l | p |   | o | y |   | l | j |
| `11000` | **x** |   | t | v |   | y | d |   | q | m |
| `11001` | **y** |   | b | c |   | w | x |   | r | p |
| `11010` | **z** |   | c | s |   | v | i |   | e | o |

>[!Note]
>**Para ler esses cifras se deve ter como base o seguinte:**
>Entrando a letra A em um rotor com a cifra A a saida será G, de modo que se entrar a letra G em um rotor inverso com a cifra A inversa a saida será A

### Tabela de Letras Minúsculas e Valores (ASCII)

| Letra | Binário | Hexadecimal |
| :---: | :---: | :---: |
| **a** | `01100001` | `0x61` |
| **b** | `01100010` | `0x62` |
| **c** | `01100011` | `0x63` |
| **d** | `01100100` | `0x64` |
| **e** | `01100101` | `0x65` |
| **f** | `01100110` | `0x66` |
| **g** | `01100111` | `0x67` |
| **h** | `01101000` | `0x68` |
| **i** | `01101001` | `0x69` |
| **j** | `01101010` | `0x6A` |
| **k** | `01101011` | `0x6B` |
| **l** | `01101100` | `0x6C` |
| **m** | `01101101` | `0x6D` |
| **n** | `01101110` | `0x6E` |
| **o** | `01101111` | `0x6F` |
| **p** | `01110000` | `0x70` |
| **q** | `01110001` | `0x71` |
| **r** | `01110010` | `0x72` |
| **s** | `01110011` | `0x73` |
| **t** | `01110100` | `0x74` |
| **u** | `01110101` | `0x75` |
| **v** | `01110112` | `0x76` |
| **w** | `01110111` | `0x77` |
| **x** | `01111000` | `0x78` |
| **y** | `01111001` | `0x79` |
| **z** | `01111010` | `0x7A` |

>[!Caution]
>Esse projeto só codifica letra minuscula, letras maiusculas passam direto para a saida


## 🚀 Como usar
1. Faça o download do [Logisim Evolution](https://github.com/logisim-evolution/logisim-evolution)
2. Faça o clone ou download desse repositorio
3. Siga as [Instruções de Usos](https://github.com/viniciussbrg/maquina_enigma/tree/main/Enigma#instru%C3%A7%C3%B5es-de-usos)

## 📺 Link para video no Youtube
>[![Maquina Enigma no Logisim](https://img.youtube.com/vi/iNSpgeBGhbU/0.jpg)](https://www.youtube.com/watch?v=iNSpgeBGhbU)

## 🌱 Melhorias a se fazer
* Adicionar mais rotores 
* Ajustar o sistema para funcionar tambem com letras maiusculas
* Ajustar o sistema para funcionar com cifras de tipos diferentes em cada rotor
* Arrumar bugs na decodificação

## 👨‍💻 Integrantes
[![GitHub](https://img.shields.io/badge/GitHub-TaysonMoises-24292e?style=flat&logo=github)](https://github.com/Tayson-M)
[![GitHub](https://img.shields.io/badge/GitHub-GuilhermeMattos-0366d6?style=flat&logo=github)](https://github.com/guilhermeomattos)
[![GitHub](https://img.shields.io/badge/GitHub-LuigiGuilherme-28a745?style=flat&logo=github)](https://github.com/luigi-guilherme)
[![GitHub](https://img.shields.io/badge/GitHub-PauloCarvalho-6f42c1?style=flat&logo=github)](https://github.com/paulohcarvalho07)
[![GitHub](https://img.shields.io/badge/GitHub-PedroCarvalho-005f73?style=flat&logo=github)](https://github.com/PedroHHCarvalho)



