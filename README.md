
**UNIVERSIDADE LUSÓFONA DE HUMANIDADES E TECNOLOGIAS**


# Exercício #3 - Billboard

Na resolução deste trabalho deve ser utilizada a Linguagem de Programação C. Para além da correta implementação dos requisitos, tenha em conta os seguintes aspetos:
- O código apresentado deve ser bem indentado. 
- O código deve compilar sem erros ou *warnings* utilizando o *gcc* com as seguintes flags:
 `-Wall -ansi -Wextra -Wpedantic`
- Tenha em atenção os nomes dados das variáveis, para que sejam indicadores daquilo que as mesmas vão conter.
- Evite o uso de constantes mágicas. 
- Evite duplicação de código. 
- Considere a implementação de funções para melhorar a legibilidade, evitar a duplicação e criar soluções mais genéricas.
- É proíbida a utilização de variáveis globais - i.e. variáveis declaradas fora de qualquer função.

## 1. Introdução

Implemente um programa que recebe um número `n` e uma string e aplica uma deslocação de `n` caracteres para a direita (`n`>0) ou para a esquerda (`n`<0). O programa deverá ler do stdin um input com o seguinte formato:
`<op> <n> <texto>`
onde

* `<op>`: é um caracter que especifica o comportamento do programa:
   - `r` : o programa deverá aplicar ao `<texto>` a deslocação de `n` caracteres para a esquerda ou para a direita e em seguida apresentar o resultado na consola.
   - `h` : deverá imprimir no terminal o resultado da última deslocação efectuada
   - `q` : o programa deverá terminar, apresentando a mensagem: `Exiting->`
* `<n>`: Indica o número de caracteres de deslocamento a aplicar.
* `<texto>`: é uma string, com o máximo de 166 caracteres, que pode conter espaços.

Uma deslocação de `n` caracteres consiste em mover os caracteres todos de uma string para as a posições contíguas e em que os últimos caracteres da string passam para o início.

Após efectuada uma operação, o programa deverá voltar a ficar à espera que o utilizador volte a introduzir uma opção. O programa apenas termina quando o utilizador introduzir a opção `q`.

Caso o utilizador introduza uma opção inexistente, programa deverá imprimir a mensagem de erro `Error: Unknown option`. 

Comece por implementar o deslocamento de um caracter para a direita. Poderá depois implementar o deslocamento de `n` caracteres para a direira repetindo `n` vezes a deslocação de `1` caracter. Repita o processo para os deslocamentos para a esquerda.

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
q
Exiting->
```

## Material a entregar

* Ficheiro `.c` com código devidamente comentado e indentado:
    - Deve implementar as funcionalidades pedidas.
    - O código deverá ser submetido na plataforma PANDORA [(2)](#ref2) até às **23:59 do dia 30 de Março de 2021** no *contest* **LP12021EX3**.
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
