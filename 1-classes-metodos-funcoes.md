# Classes  

- O arquivo que terá uma classe não precisa ter o mesmo nome dela;  
- O arquivo pode ter extensão `.scala ou .sc`;  
- A classe depois de compilada será transformada em Bytecode. Isso pode ser verificado com `javap -p minhaClasse`;  
- O mínimo para se criar uma classe é colocar a declaração `class MinhaClasse`;  
- A JVM exite que para ser executado, um código deve ter um método main com um array de strings;  
- Uma classe é instanciada com a declaração da claúsula `new NomeDaClasse`;  
- Por padrão uma classe sempre é pública;  
- Por padrão todo atributo de uma classe é privado.  
- É possível usar subconstrutores. Mas é necessário chamar o construtor principal;  



## Exemplos de Classe  

* Classe sem construtor:  

```scala
class MinhaClasse
```  

* Classe com construtor:  

```scala
class MinhaClasse(x:Int, y:String)
```  

* Classe com bloco:  

```scala
class MinhaClasse{
}
```  


* Instânciando uma classe:  

```scala
class MinhaClasse{
}

val x = new MinhaClasse

println(x.toString)
println(x.getClass)
println(x.hashCode)
```  

* Classe com construtor e subconstrutor:  

```scala
class MinhaClasse(x:Int, y:String){
    def this() = this(0, "")
}

val a = new MinhaClasse()
val b = new MinhaClasse(1, "Scala") 
```  

* Classe com construtor e vários subconstrutores:  

```scala
class MinhaClasse(x:Int, y:String){
    def this(x:Int, y:String, z:Double) = this(x, y)
    def this() = this(0, "")    
}

val a = new MinhaClasse()
val b = new MinhaClasse(1, "Scala") 
val c = new MinhaClasse(1, "Scala", 9.9) 
```  

* Criando atributos de uma classe direto pelo construtor(através de `var` e `val`):  

Se for criado com val, será imultável(constante). Só terá getters(implicito).  
Se for criado com var, será multável(variável). Terá getters e setters(implicitos).  

```scala
class MinhaClasse(var x:Int, val y:String){
}

val a = new MinhaClasse(1, "Scala")

a.x = 110      // Setter implícito.

println(a.x)  // 110   -  Getter implíto.
println(a.y)  // Scala -  Getter implíto.
```  

# Executando Código  

É possível extender a classe `App` que permite executarmos algum código de forma mais rápida, sem precisar criar um método main. É uma alternativa boa para fazer testes.  

O `object` em Scala `é uma classe`, que ao mesmo tempo, é o `próprio objeto`. É um `Singleton` da sua própria classe. O `object` funciona como uma mistura do `final` e `static` do Java. São instâncias das suas próprias definições.  

```scala
object Teste extends App{
  println("Olá Mundo")
}
```  

* Usando `object` para executar uma classe

```scala
class MinhaClasse(){
    val PI = 3.14
}

object Teste extends App{
    val minhaClasse = new MinhaClasse
    println(minhaClasse.PI)
}

// No terminal digite:
// scala nome-do-arquivo.scala
```  

* Executando uma classe no terminal

```scala
class MinhaClass{  
  def imprimirPI() : Unit = { // Unit equivale como o retorno void do Java.
    println(3.14)
  }
}

val mc = new MinhaClasse
mc.imprimirPI()

// No terminal digite:
// scala nome-do-arquivo.scala
```
