# Classes  

- O arquivo que terá uma classe não precisa ter o mesmo nome dela;  
- O arquivo pode ter extensão `.scala ou .sc`;  
- A classe depois de compilada será transformada em Bytecode. Isso pode ser verificado com `javap -p minhaClasse`;  
- O mínimo para se criar uma classe é colocar a declaração `class MinhaClasse`;  
- A JVM exite que para ser executado, um código deve ter um método main com um array de strings;  
- Uma classe é instanciada com a declaração da claúsula `new NomeDaClasse`;  


## Exemplos de Classe  

* Classe sem construtor:  

```scala
class MinhaClasse
```  

* Classe com construtor:  

```scala
class MinhaClasse(x:Int, y:String)
```  

