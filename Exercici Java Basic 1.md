**Pregunta1**<br />
**Declara dues variables de tipus byte, b0 i b1, i assigna-lis respectivament els valors 122 i 14.<br />
Suma les dues variables, sense assignar el resultat a cap variable (jshell l'assignarà automàticament a un variable temporal, que comença per $):<br />**
```
byte b0 = 122;
byte b1 = 14;
System.out.println(b0 + b1);
```
```
136
```
**Quin resultat obtenim? Per què? De quin tipus de dada és la variable temporal creada pel notebook?**<br/>
Obtenim la suma de les dos variables correctament, la dada que crea el notebook com a resultat és un tipus de número int. <br />

**Pregunta 2** <br />
**Declara una variable de tipus char anomenada c, i assignali el valor 'a'. <br />
Declara una variable tipus int, anomenada n, i assignali el valor de la variable c. <br />
Quin resultat obtens? Per què?**
```
char c = 'a';
int n = c;
System.out.printf("%c%n%d%n", c, n);
```
```
a
97
```
Ens dona aquest resultat ja que estem assignant a la variable n el valor de la variable c, en aquest cas el valor és 'a'. En el codi ASCII la lletra 'a' te com a valor el número 97 que és el número que esta assignant a la variable n. <br />
**Ara, declara una variable de tipus short, anomenada s, i assigna-li el valor de la variable c:**<br />
```
char c = 'a';
short s = c;
System.out.printf("%c%n%d%n", c, s);
```
**Per què ara el resultat obtingut és diferent que en el cas anterior?**<br />
En aquest cas ens dona error ja que te incompatibilitat de la conversió de tipus char a short.<br />

**Pregunta 3<br />
Continuant amb les variables de tipus char i short declarades a l'exercici 2, ara executeu:**
```
char c = 'a';
short s = (short)c;
System.out.printf("%c%n%d%n", c, s);
```
```
a
97
```
**Com s'anomena això que estem fent amb la variable c? Quin resultat obtenim ara? Per què (què està passant)?**<br />
El que estem fent és un casting, és a dir estem assegurant que el valor de aquesta variable sigui definida totalmant com a dada tipus short. El resultat que obtenim éS el resultat de la lleta en números per el sistem ASCII. <br />

**Pregunta 4<br />
Executa el següent codi en una cel·la del notebook:**
```
short s0 = (short)32000;
short s1 = (short)35000;
System.out.printf("%d%n%d%n", s0, s1);
```
```
32000
-30536
```
Dona aquest resultat ja que el rang que te el tipus short no pot incluir aquest número per tant el notebook amb els bytes que hi ha ho fica<br />

**Pregunta 5 <br />
Executa el següent codi amb el jshell:**<br />
```
var v = 5.0;
var v0 = 5;
System.out.printf("%1.1f%n%d%n", v, v0)
```
```
5.0
5
```
**De quin tipus de dada són les variables v i v0?**<br />
El tipus de dada var és un tipus de variable que es automàtica, en aquest cas es detecta que v = tipus de dada flotant i v0 = tipus de dad int.<br />
**Ara executa:**
```
var v = 5.0;
var v0 = 5;
var v1 = v + v0;
System.out.printf("%1.2f + %d = %1.2f%n", v, v0, v1)
```
```
5.00 + 5 = 10.00
```
**De quin tipus de dada és la variable v1? Per què (què està passant en fer-se la suma)?**<br />
La variable és tipus com flotant ja que hi ha una variable de la suma que és tipus float llavors ens dona el resultat amb coma flotant.<br />

**Pregunta 8**<br />
**Declareu dues variables de tipus char de la següent manera char c = 'a', c1 = 1;<br />
L'objectiu d'aquest exercici és assignar el valor 'b' en una tercera variable de tipus char, però sense usar el literal 'b', sinó fent la suma de les variables c i c1, és a dir: char c2 = c + c1;**
```
char c = 'a';
char c1 = 1;
char c2 = c + c1;
System.out.printf("%c%n", c2 );
```
```
char c2 = c + c1;
incompatible types: possible lossy conversion from int to char
```
**Què està passant? Com ho podem solucionar per tal d'aconseguir l'objectiu d'aquest exercici?**<br />
El que pasa com es veu a l'error és que no pot fer una correcta conversió de la dada int a char. Per conseguir que aquesta suma surti correctament hem de fer un casting per tal de fer que aquesta dada que consider int sigui char.
```
char c = 'a';
char c1 = 1;
char c2 = (char)(c + c1);
System.out.printf("%c%n", c2 );
```
```
b
```

**Pregunta 9**<br />
**Executa la següent expressió i assigna-la a una variable h:
var h = 4 * 4f + (4.0 + 4); <br />
Ara, assigna el valor guardat a la variable h, a una altra variable de tipus float:
float f = h;**<br />
```
var h = 4 * 4f + (4.0 +4);
float f = h;
System.out.printf("%f%n", f)
```
```
 float f = h;
incompatible types: possible lossy conversion from double to float
```
**Què obtenim? Per què?**<br />
Obtenim un problema de conversió de dades ja que el reslutat que obtenim és un tipus de dada double i no float.<br />
**Ara escriu el canvi que cal fer en l'expressió incial (4*4f + (4.0 + 4)) per tal que l'assignació del valor d'h a f sigui reeixit.**<br />
Cal fer un casting per tal de que ens doni el resultat de la operació:
```
var h = (4 * 4f + (4.0 +4));
float f = (float)h;
System.out.printf("%1.2f%n", f)
```
```
24.00
```
**Pregunta 10**<br />
**A partir de les següents variables i assignacions byte b0 = 4, b1 = -4, b2 = 12;. Executa el següent codi** 
```
boolean bol1 = b0 == b2 / 3;
boolean bol2 = b0 + b1;
boolean bol3 = b0 + b1 > b2;
```

**Explica els resultat obtinguts en cada cas:**<br />
En el primer cas obtenim el resultat trues ja que estem dividint b2 que es 12 entre 3 que és igual a 4 que és el mateix número que b0.
```
byte b0 = 4, b1 = -4, b2 = 12;
boolean bol1 = b0 == b2 / 3;
System.out.printf("Resultat boolean 1 = %b%n", bol1)
```
```
Resultat boolean 1 = true
```
En el sgeon cas obtenim un error ja que a la varibale bol2 estem fent una suma a dos tipus de dades booleanes sense cap signe de comparació per tant el resultat que surt en cas de que no fos un error és un número enter.

```
byte b0 = 4, b1 = -4, b2 = 12;
boolean bol2 = b0 + b1;
System.out.printf("Resultat boolean 2 = %b%n", bol2)
```
```
boolean bol2 = b0 + b1;
incompatible types: int cannot be converted to boolean
```
En el tercer i últim cas obtenim el resultat false ja que estem sumant b0 que i b1 que dona com a resultat 0 i a la variable bol3 estem fent un comparació b0 més gran que b2 que te com a valor 12 ens dona el resultat false.
```
byte b0 = 4, b1 = -4, b2 = 12;
boolean bol3 = b0 + b1 > b2;
System.out.printf("Resultat boolean 3 = %b%n", bol3)
```
```
Resultat boolean 3 = false
```
