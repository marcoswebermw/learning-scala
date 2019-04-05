# Introdução  

Scala é interoperável com Java(não é uma extensão dela), por isso usa as bibliotecas padrão do Java.  

Salve um arquivo com extensão `.scala` e rode o comando `scalac ola_mundo.scala` para compilar em ByteCode. 
Depois execute o `scala meu_programa` para executá-lo.  

```scala
// Arquivo ola_mundo.scala
class Teste
```  

## Declarando Variáveis  

Se não for passado o tipo da variável o compilador vai inferir. Scala tem tipagem forte.  
Scala aceita simbolos alguns como `& $ ?` funcionando como identificador de variáveis e constantes(Java não aceita).  

```scala
// Declarando variável.
var linguagem1 = "Scala"

// Declarando variável e indicando tipo.
// São usados os dois pontos, o tipo, e depois o sinal de igual para atribuição.
var linguagem2: String = "Java"

// É o mesmo println do pacote java.lang.
println(linguagem1) // Scala
println(linguagem2) // Java
println("A linguagem " + linguagem1 + " não é uma extensão do " + linguagem2)  
// A linguagem Scala não é uma extensão do Java
```  

## Declarando Constantes  

Diferente do Java que usa a palavra reservada `final` o Scala usa `val` para constantes. 
Uma constante não pode ter seu valor reatribuído. De resto é similar ao `var`.  

```scala
// Declarando constante.
val linguagem1 = "Scala"

// Declarando constante e indicando tipo.
// São usados os dois pontos, o tipo, e depois o sinal de igual para atribuição.
val linguagem2: String = "Java"

// É o mesmo println do pacote java.lang.
println(linguagem1) // Scala
println(linguagem2) // Java
println("A linguagem " + linguagem1 + " não é uma extensão do " + linguagem2)  
// A linguagem Scala não é uma extensão do Java
```  
