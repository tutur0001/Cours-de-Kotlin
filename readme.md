Cours de Kotlin  
==
### Déclaration de variable:  
En kotlin il y a plusieurs manière de déclarer une variable 
l'exemple ci dessous montre trois façon de déclarer une variable de type "String" :
`val nomDeLaVariable = "Hello World `
`val nomDeLaVariable:String = "Hello world`
`var nomDeLaVariable:String = "Hello world`

`val` (pour valeur): Sera une variable immuable, vous ne pourrez pas la modifier une fois initialisées.
`var` (pour variable): Sera muable, vous pourrez la modifier même après l'avoir initialisé.

Kotlin invite fortement a déclarer nos variable en immuable afin de rendre notre code le plus proche possible du style de programmation fonctionnelle, limitant ainsi l'effets de bord.
En revanche les variables avec le mot-clé `val` n'on pas obligation d'etre declarer dans le meme bloc !

Exemple:

    val message:String 
    if (UserHappy()){
	    message = "Je suis content"
	} else {
		message = "je suis mécontent ! " 
	}    

#### NULL SAFETY :

En kotlin ils nous aient permit de declarer une variable a null, 
pour cela rien de bien compliquer il suffit juste de l'écrire comme cela:  

	var message:String? = "Cette variable peut etre null"
	message.toUppercase()
#### Les constantes : 

En kotlin le mot-clé `static` n'existe plus, il existe tout de meme un equivalent 

Ainsi, voici l'equivalent sous kotlin :

`
const val SERVER_URL: string="https://myapi.com"` 
 le mot-clé `const` suivi du mots-clé `val` permet de définir une constante dont la valeur sera connu au moment de la compilation.
#### Petit tips: 
Imaginons que nous voulions declarer une variable muable mais que nous souhaitons pas l'initialiser immédiatement mais plus tard dans le code.
Nous pouvons faire comme cela : 
`var username: String = null`
cela peu marcher sauf que votre variable peu etre possiblement null et nous ne voulons pas.
Dans ce cas il faut utiliser simplement `lateinit`(pour "late-initialized").
Cela permet d'indiquer a kotlin que vous etes sur et certain d'initialiser la variable en question un peu plus tard dans notre code.
exemple:  

	lateinit var username: String
	
	var name: String = "Jon" 
	println(name)
	username = "patrick" 


### Implémenter différentes fonctions:

Décortiquons cette fonctions:  
    
    fun main(args: Array<String>) {
    println("helloà world")
    }
Expliquons un peu plus en détail ces lignes :
* Le mot-clé `fun`suivi de son nom nous permet de définir une fonction, puis de la nommer.
* Le type du paramètre (`Array<String>`) est indiquer après son nom (`args`). Les deux point `:` indiquent toujours la déclaration d'un type en kotlin.
* Une fonction pet se déclarer dans un fichier Kotlin (possédant l'extension .kt) sans etre a l'intérieur d'une classe. Nous en parlerons en details un peu plus tard.
* Nous afficherons dans la console du texte grace a la commande `println()`. C'est l'équivalent du fameux `System.out.println` en java.
* La encore, vous n'avez pas besoins d'ajouter un point virgule pour terminer votre instruction.

#### Fonction un peu plus complexe:

![fun picture](https://user.oc-static.com/upload/2018/05/25/15272618306081_kotlin_function_medium.png)

Comme on peut le remarquer juste au dessus, les paramètres de la fonction sont séparés par une virgule.
Afin de retourner une valeur de type `Int`
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTIyNTg1MjE4MSwtMTI2Nzg4OTg1MywtMT
M4MTM1MTc2OV19
-->