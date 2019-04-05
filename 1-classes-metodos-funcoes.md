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

