**Pregunta 1<br />
Declara dues variables de tipus byte, b0 i b1, i assigna-lis respectivament els valors 122 i 14.<br />
Suma les dues variables, sense assignar el resultat a cap variable (jshell l'assignarà automàticament a un variable temporal, que comença per $):<br />
Quin resultat obtenim? Per què? De quin tipus de dada és la variable temporal creada pel notebook?**
```
byte b0 = 122;
byte b1 = 14;
System.out.println(b0 + b1);
```
```
136
```

**Pregunta 2 <br />
Declara una variable de tipus char anomenada c, i assignali el valor 'a'. <br />
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
**TODO**<br />
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
**TODO**<br />
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
