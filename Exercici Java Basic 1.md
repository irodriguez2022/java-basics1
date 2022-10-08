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
En aquest cas de la variable int ens dona el resultat de un número ja que en el codi ASCII el resultat obtingut de la 'a' és el número 97.<br />
Ara, declara una variable de tipus short, anomenada s, i assigna-li el valor de la variable c:<br />
