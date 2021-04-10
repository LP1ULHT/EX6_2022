
**UNIVERSIDADE LUSÓFONA DE HUMANIDADES E TECNOLOGIAS**


# Exercício #4 - Billboard - Versão 2

Na resolução deste trabalho deve ser utilizada a Linguagem de Programação C. Para além da correta implementação dos requisitos, tenha em conta os seguintes aspetos:
- O código apresentado deve ser bem indentado. 
- O código deve compilar sem erros ou *warnings* utilizando o *gcc* com as seguintes flags:
 `-Wall -ansi -Wextra -Wpedantic`
- Tenha em atenção os nomes dados das variáveis, para que sejam indicadores daquilo que as mesmas vão conter.
- Evite o uso de constantes mágicas. 
- Evite duplicação de código. 
- Considere a implementação de funções para melhorar a legibilidade, evitar a duplicação e criar soluções mais genéricas.
- É proíbida a utilização de variáveis globais - i.e. variáveis declaradas fora de qualquer função.

**Neste problema não é permitida a utilização das bibliotecas string.h, strings.h, e stdlib.h.**
**Neste problema não é permitida a utilização das bibliotecas string.h, strings.h, e stdlib.h.**
**Neste problema não é permitida a utilização das bibliotecas string.h, strings.h, e stdlib.h.**
**Neste problema não é permitida a utilização das bibliotecas string.h, strings.h, e stdlib.h.**
**Neste problema não é permitida a utilização das bibliotecas string.h, strings.h, e stdlib.h.**
**Neste problema não é permitida a utilização das bibliotecas string.h, strings.h, e stdlib.h.**

## 1. Introdução

Implemente um programa que recebe um número `n` e uma string e aplica uma transformação de acordo com a opção escolhida pelo utilizador. O programa deverá ler do stdin um input com o seguinte formato:
`<op> <n> <texto>`
onde

* `<op>`: é um caracter que especifica o comportamento do programa:
   - `r` : o programa deverá aplicar ao `<texto>` a deslocação de `n` caracteres para a esquerda ou para a direita e em seguida apresentar o resultado na consola (ver Secção [1.1](#rot)).
   - `s` : o programa deverá aplicar ao `<texto>` a cifra de substituíção (ver Secção [2.1](#subst)) e apresentar o resultado na consola. 
   - `h` : deverá imprimir no terminal o resultado da última deslocação efectuada
   - `q` : o programa deverá terminar, apresentando a mensagem: `Exiting->`
* `<n>`: Indica o número de caracteres de deslocamento a aplicar.
* `<texto>`: é uma string, com o máximo de 166 caracteres, que pode conter espaços.

Após efectuada uma operação, o programa deverá voltar a ficar à espera que o utilizador volte a introduzir uma opção. O programa apenas termina quando o utilizador introduzir a opção `q`.

Caso o utilizador introduza uma opção inexistente, programa deverá imprimir a mensagem de erro `Error: Unknown option`. 

### 1.1 Rotação<a name="rot"></a>

Aplicar uma deslocação de `n` caracteres para a direita (`n`>0) ou para a esquerda (`n`<0). Uma deslocação de `n` caracteres consiste em mover os caracteres todos de uma string para as a posições contíguas e em que os últimos caracteres da string passam para o início.

Esta opção é igual ao que foi feito no exercício #3.

### 1.2 Cifra de substituição<a name="subst"></a>

Uma cifra de substituição é um algoritmo que permite a encriptação substituindo um dado caracter por outro. A forma como se encontra a correspondência de um caracter do alfabeto para outro pode ser definido através de um *shift* do alfabeto para a direita. Por exemplo uma cifra de substituição *5* tem a seguinte correspondência:

`0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ` - Alfabeto  
`56789ABCDEFGHIJKLMNOPQRSTUVWXYZ01234` - Alfebeto Cifrado

`CADA MALLOC PRECISA DE UM FREE` - Frase original  
`HFIF RFQQTH UWJHNXF IJ ZR KWJJ` - Frase encriptada

Nesta versão simplificada apenas os caracteres `0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ` são encriptados. Desta forma, o texto deverá ser convertido para letras maiúsculas e todos os caracteres que não pertencem ao grupo dos caracteres encriptados deverão manter-se inalterados - como é o caso dos espaços no exemplo anterior.
Caso o utilizador especifique um número positivo, o deslocamento é feito para a direita (como no caso do exemplo). Caso o número seja negativo, o deslocamento é feito para a esquerda.

O utilizador poderá introduzir o texto utilizando letras maiúsculas ou minúsculas, mas o resultado deverá ser sempre apresentado em maiúsculas.

O parâmetro `n` introduzido pelo utilizador terá obrigatoriamente que estar no intervalo [-35 ; 35]. Caso o número esteja fora do intervalo o programa deverá imprimir a seguinte mensagem de erro: `Error: out of bound` e deverá voltar a esperar um novo *input* do utilizador. 


## Exemplo de utilização do programa
```shell_session
$>./billboard
r 1 programming is the art of copy and paste.
.programming is the art of copy and paste
r 5 programming is the art of copy and paste.
aste.programming is the art of copy and p
r -5 Simplicity is prerequisite for reliability.
icity is prerequisite for reliability.Simpl
h
icity is prerequisite for reliability.Simpl
s 9 programming is the art of copy and paste.
Y0XP0JVVRWP R1 2QN J02 XO LXY7 JWM YJ12N.
q
Exiting->
```

## Material a entregar

* Ficheiro `.c` com código devidamente comentado e indentado:
    - Deve implementar as funcionalidades pedidas.
    - O código deverá ser submetido na plataforma PANDORA [(2)](#ref2) até às **23:59 do dia 18 de Abril de 2021** no *contest* **LP12021EX4**.
    - Incorrecta indentação do código poderá originar penalizações na nota.
 
## Honestidade Académica

Nesta disciplina, espera-se que cada aluno siga os mais altos padrões de honestidade académica. Trabalhos que sejam identificados como cópias serão anulados e os alunos envolvidos terão nota zero - quer tenham copiado, quer tenham deixado copiar.
Para evitar situações deste género, recomendamos aos alunos que nunca partilhem ou mostrem o seu código.
A decisão sobre se um trabalho é uma cópia cabe exclusivamente aos docentes da unidade curricular.
Os alunos são encorajados a discutir os problemas com outros alunos mas não deverão, no entanto, copiar códigos, documentação e relatórios de outros alunos. Em nenhuma circunstância deverão partilhar os seus próprios códigos, documentação e relatórios. De facto, não devem sequer deixar códigos, documentação e relatórios em computadores de uso partilhado.

## Referências

<a name="ref1"></a>

* (1) Pereira, A. (2017). C e Algoritmos, 2ª edição. Sílabo.

<a name="ref2"></a>

* (2)  PANDORA - Yet Another Automated Assessment Tool, https://saturn.ulusofona.pt/.

## Metadados

* Autor: [Pedro Serra, Lúcio Studer, Guilherme Sanches, Tiago Simas]
* Curso:  [Licenciatura em Engenharia Informática][lei]
* Curso:  [Licenciatura em Engenharia Informática e Redes de Telecomunicações][leirt]
* Curso:  [Licenciatura em Informática de Gestão][lig]
* Instituição: [Universidade Lusófona de Humanidades e Tecnologias][ULHT]
