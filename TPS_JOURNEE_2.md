# Exercices

## 1.BOUCLES

### TP1

Ecrire un algorithme qui demande un nombre de départ, et qui ensuite écrit la table de multiplication de ce nombre, présentée comme suit (cas où l'utilisateur entre le nombre 7) :
Table de 7 :

7 x 1 = 7
7 x 2 = 14
7 x 3 = 21
…
7 x 10 = 70

```js
// V1
FONCTIONS_UTILISEES

VARIABLES
nb EST_DU_TYPE NOMBRE
counter EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
LIRE nb
POUR counter ALLANT_DE 1 A 10
	DEBUT_POUR
	AFFICHER nb
	AFFICHER " x "
	AFFICHER counter
	AFFICHER " = "
	AFFICHERCALCUL* nb*counter
	FIN_POUR
FIN_ALGORITHME
```

```js
// V2
FONCTIONS_UTILISEES
VARIABLES
  chiffre EST_DU_TYPE NOMBRE
  counter EST_DU_TYPE NOMBRE
  premierMultiplicateur EST_DU_TYPE NOMBRE
  dernierMultiplicateur EST_DU_TYPE NOMBRE
  temp EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  LIRE chiffre
  SI (chiffre==0) ALORS
    DEBUT_SI
    AFFICHER "Vous devez entrer une valeur differente de 0"
    FIN_SI
    SINON
      DEBUT_SINON
      LIRE premierMultiplicateur
      LIRE dernierMultiplicateur

      SI (premierMultiplicateur > dernierMultiplicateur) ALORS
        DEBUT_SI
        temp PREND_LA_VALEUR premierMultiplicateur
        premierMultiplicateur PREND_LA_VALEUR dernierMultiplicateur
        dernierMultiplicateur PREND_LA_VALEUR temp
        FIN_SI
      POUR counter ALLANT_DE premierMultiplicateur A dernierMultiplicateur
        DEBUT_POUR
        AFFICHER chiffre
        AFFICHER " x "
        AFFICHER counter
        AFFICHER " = "
        AFFICHERCALCUL* chiffre*counter
        FIN_POUR
      FIN_SINON
FIN_ALGORITHME

```

```js
V3 Méthode de complément


//a = a + b
//b = a - b (À cette étape, b devient la valeur originale de a)
//a = a - b (Maintenant, a prend la valeur originale de b)

// a = 2
// b = 1

// a = a+b => 2+1 => 3
// b = a-b => 3 - 1 => 2
// a = a-b => 3 - 2 => 1


FONCTIONS_UTILISEES
VARIABLES
  chiffre EST_DU_TYPE NOMBRE
  counter EST_DU_TYPE NOMBRE
  premierMultiplicateur EST_DU_TYPE NOMBRE
  dernierMultiplicateur EST_DU_TYPE NOMBRE
  temp EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  LIRE chiffre
  SI (chiffre==0) ALORS
    DEBUT_SI
    AFFICHER "Vous devez entrer une valeur differente de 0"
    FIN_SI
    SINON
      DEBUT_SINON
      LIRE premierMultiplicateur
      LIRE dernierMultiplicateur

      SI (premierMultiplicateur > dernierMultiplicateur) ALORS
        DEBUT_SI
        premierMultiplicateur PREND_LA_VALEUR premierMultiplicateur + dernierMultiplicateur
        dernierMultiplicateur PREND_LA_VALEUR premierMultiplicateur - dernierMultiplicateur
        premierMultiplicateur PREND_LA_VALEUR premierMultiplicateur - dernierMultiplicateur
        FIN_SI
      POUR counter ALLANT_DE premierMultiplicateur A dernierMultiplicateur
        DEBUT_POUR
        AFFICHER chiffre
        AFFICHER " x "
        AFFICHER counter
        AFFICHER " = "
        AFFICHERCALCUL* chiffre*counter
        FIN_POUR
      FIN_SINON
FIN_ALGORITHME

```

### TP2
Ecrire un algorithme qui permettra de calculer plusieurs tables de multiplication.

On va d’abord demander à l’utilisateur de saisir le 1er nombre dont il faut connaître la table de multiple, ensuite on lui demandera le dernier nombre.

Si par exemple le premier nombre est 3 et le dernier 8, on va afficher toutes les tables de multiplications de 3 à 8, donc : 3,4,5,6,7,8

Après on demandera à l’utilisateur d’entre le premier nombre et le dernier nombre à multiplier.

Si par exemple il saisit comme premier nombre 3 et dernier nombre 7, on aura;

3 x 3 = 9  4 x 3 = 12 …  8 x 3 = 24
3 x 4 = 12  4 x 4 = 14 …  8 x 4 = 32
3 x 5 =15  4 x 5 = 20 …  8 x 5 = 40
3 x 6 = 18  4 x 6 = 24 …  8 x 6 = 48
3 x 7 = 21  4 x 7 = 28 …  8 x 7 = 56

```js
FONCTIONS_UTILISEES
VARIABLES
  premierNombre EST_DU_TYPE NOMBRE
  dernierNombre EST_DU_TYPE NOMBRE
  premierMultiplicateur EST_DU_TYPE NOMBRE
  dernierMultiplicateur EST_DU_TYPE NOMBRE
  i EST_DU_TYPE NOMBRE
  j EST_DU_TYPE NOMBRE
  temp EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  AFFICHER* "Entrez le premier nombre pour la table de multiplication :"
  LIRE premierNombre
  AFFICHER* "Entrez le dernier nombre pour la table de multiplication :"
  LIRE dernierNombre
  SI (premierNombre > dernierNombre) ALORS
    DEBUT_SI
    temp PREND_LA_VALEUR premierNombre
    premierNombre PREND_LA_VALEUR dernierNombre
    dernierNombre PREND_LA_VALEUR temp
    FIN_SI
  AFFICHER* "Entrez le premier multiplicateur :"
  LIRE premierMultiplicateur
  AFFICHER* "Entrez le dernier multiplicateur :"
  LIRE dernierMultiplicateur
  SI (premierMultiplicateur > dernierMultiplicateur) ALORS
    DEBUT_SI
    temp PREND_LA_VALEUR premierMultiplicateur
    premierMultiplicateur PREND_LA_VALEUR dernierMultiplicateur
    dernierMultiplicateur PREND_LA_VALEUR temp
    FIN_SI
  POUR i ALLANT_DE premierNombre A dernierNombre
    DEBUT_POUR
    POUR j ALLANT_DE premierMultiplicateur A dernierMultiplicateur
      DEBUT_POUR
      AFFICHER i
      AFFICHER " x "
      AFFICHER j
      AFFICHER " = "
      AFFICHERCALCUL* i * j
      FIN_POUR
    AFFICHER* "----------"
    FIN_POUR
FIN_ALGORITHME
```


### TP3
Ecrivez un programme qui affiche en console les nombres de 1 à n:

pour les multiples de trois, il affiche "fizz" à la place du nombre
et pour les multiples de cinq de cinq, imprimez "buzz".
Pour les nombres qui sont des multiples multiples à la fois de trois et de cinq, imprimez "fizzbuzz".
Sinon, il affiche le nombre

Exemple
Si n = 5
1
2
fizz
4
Buzz

```js
FONCTIONS_UTILISEES
VARIABLES
  nbr EST_DU_TYPE NOMBRE
  compteur EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  LIRE nbr
  POUR compteur ALLANT_DE 1 A nbr
    DEBUT_POUR
    SI (compteur%3==0 ET compteur%5==0) ALORS
      DEBUT_SI
      AFFICHER compteur
      AFFICHER* "- FizzBuzz"
      FIN_SI
      SINON
        DEBUT_SINON
        SI (compteur%3==0) ALORS
          DEBUT_SI
          AFFICHER compteur
          AFFICHER* "- Fizz"
          FIN_SI
          SINON
        SI (compteur%5==0) ALORS
          DEBUT_SI
          AFFICHER compteur
          AFFICHER* "- Buzz"
          FIN_SI
          SINON
            DEBUT_SINON
            AFFICHER* compteur
            FIN_SINON
        FIN_SINON
    FIN_POUR
FIN_ALGORITHME
```


### TP4
Écrivez un programme Java qui demande à l’utilisateur d’entrer un nombre et qui ensuite va calculer et afficher la factorielle de ce nombre:

Ex:

Nombre : 3

Factorielle de 3 : 1x2x3= 6

```js
FONCTIONS_UTILISEES
VARIABLES
facto EST_DU_TYPE NOMBRE
counter EST_DU_TYPE NOMBRE
n EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
LIRE n
SI (n<0) ALORS
	DEBUT_SI
	AFFICHER "La factorielle d'un nombre négatif n'est pas définie."
	FIN_SI
	SINON
		DEBUT_SINON
		SI (n==0 || n==1) ALORS
			DEBUT_SI
			AFFICHER "La factorielle de "
			AFFICHER n
			AFFICHER " est 1"
			FIN_SI
			SINON
				DEBUT_SINON
				facto PREND_LA_VALEUR 1
				POUR counter ALLANT_DE 1 A n
					DEBUT_POUR
					facto PREND_LA_VALEUR facto*counter
					FIN_POUR
					AFFICHER "La facotielle de "
					AFFICHER n
					AFFICHER " est "
					AFFICHER facto
				FIN_SINON
		FIN_SINON
FIN_ALGORITHME

```


### TP 5
Écrire un algorithme qui permet à l’utilisateur de définir une adresse email et un mot de passe.

Ensuite dans un second temps, il sera demandé à l’utilisateur de fournir l’email et le mot de passe:

Si l’email et le mot de passe ne correspondent pas aux valeurs définies, le message “Identifiants incorrects devra s’afficher”, et l’utilisateur devra recommencer la saisie des valeurs.
Sinon, le message “Bienvenu dans votre espace client” devra s’afficher.

Le nombre de fois que l’utilisateur peut saisir des mauvais identifiants est limité à 5, ensuite le programme va s’arrêter avec un message disant

“Vous avez saisi des mauvais identifiants x fois, votre compte est bloqué”.

```js
FONCTIONS_UTILISEES
VARIABLES
  email EST_DU_TYPE CHAINE
  password EST_DU_TYPE CHAINE
  loginEmail EST_DU_TYPE CHAINE
  loginPassword EST_DU_TYPE CHAINE
  attempts EST_DU_TYPE NOMBRE
  areInputsValid EST_DU_TYPE CHAINE
DEBUT_ALGORITHME
  LIRE email
  LIRE password
  areInputsValid PREND_LA_VALEUR "no"
  attempts PREND_LA_VALEUR 1
  TANT_QUE ((loginEmail!=email OU loginPassword!=password) ET attempts<=5) FAIRE
    DEBUT_TANT_QUE
    LIRE loginEmail
    LIRE loginPassword
    attempts PREND_LA_VALEUR attempts + 1
    SI (loginEmail!=email OU loginPassword!=password) ALORS
      DEBUT_SI
      AFFICHER* "Identifiants incorrects."
      FIN_SI
    SI (loginEmail==email ET loginPassword==password) ALORS
      DEBUT_SI
      areInputsValid PREND_LA_VALEUR "yes"
      FIN_SI
    FIN_TANT_QUE
  SI (areInputsValid=="yes") ALORS
    DEBUT_SI
    AFFICHER "Bienvenue dans votre espace client."
    FIN_SI
    SINON
      DEBUT_SINON
      AFFICHER "Vous avez saisi des mauvais identifiants"
      AFFICHER attempts
      AFFICHER " fois, votre compte est bloqué"
      FIN_SINON
FIN_ALGORITHME
```

## TP 6
Écrire un algorithme qui demande à l’utilisateur un nombre compris entre 1 et 3 jusqu’à ce que la réponse convienne.
```js
FONCTIONS_UTILISEES
VARIABLES
  nbr EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  TANT_QUE (nbr<1 OU nbr>3) FAIRE
    DEBUT_TANT_QUE
    LIRE nbr
    SI (nbr>=1 ET nbr<=3) ALORS
      DEBUT_SI
      AFFICHER "Trouve"
      FIN_SI
      SINON
        DEBUT_SINON
        AFFICHER "Saisie invalide, le nombre doit etre compris entre 1 et 3."
        FIN_SINON
    FIN_TANT_QUE
FIN_ALGORITHME
```


### TP  7
Écrire un algorithme qui demande à l’utilisateur une chaîne, et ensuite lui retourne le nombre des voyelles et consonnes contenu dans la chaîne.

Exemple:

Entrée : Benjamin

Résultat : 3 voyelles, 5 consonnes

```js
FONCTIONS_UTILISEES
VARIABLES
  mot EST_DU_TYPE CHAINE
  voyelles EST_DU_TYPE NOMBRE
  consonnes EST_DU_TYPE NOMBRE
  caractere EST_DU_TYPE CHAINE
  i EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  LIRE mot
  voyelles PREND_LA_VALEUR 0
  consonnes PREND_LA_VALEUR 0
  POUR i ALLANT_DE 0 A mot.length-1
    DEBUT_POUR
    caractere PREND_LA_VALEUR mot.substr(i, 1)
    SI (caractere=="a" OU caractere=="e" OU caractere=="i" OU caractere=="o" OU caractere=="u" OU caractere=="y" OU caractere=="A" OU caractere=="E" OU caractere=="I" OU caractere=="O" OU caractere=="U" OU caractere=="Y") ALORS
      DEBUT_SI
      voyelles PREND_LA_VALEUR voyelles + 1
      FIN_SI
    SINON
      DEBUT_SINON
      consonnes PREND_LA_VALEUR consonnes + 1
      FIN_SINON
    FIN_POUR
  AFFICHER "Résultat : "
  AFFICHER voyelles
  AFFICHER " voyelles, "
  AFFICHER consonnes
  AFFICHER " consonnes"
FIN_ALGORITHME
```

### TP 8
Écrire un algorithme qui demande à l’utilisateur une chaîne, et ensuite un caractère, puis lui retourne le nombre de fois que le caractère saisi se trouve dans la chaîne et dire si c’est une voyelle ou une consonne.

Exemple:

Caractère : i
chaine : christian

Résultat : i se retrouve 2 fois, et c’est une voyelle

```js
FONCTIONS_UTILISEES
VARIABLES
  mot EST_DU_TYPE CHAINE
  caractereRecherche EST_DU_TYPE CHAINE
  occurences EST_DU_TYPE NOMBRE
  i EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  LIRE mot
  LIRE caractereRecherche
  occurences PREND_LA_VALEUR 0
  POUR i ALLANT_DE 0 A mot.length-1
    DEBUT_POUR
    SI (mot.substr(i, 1) == caractereRecherche) ALORS
      DEBUT_SI
      occurences PREND_LA_VALEUR occurences + 1
      FIN_SI
    FIN_POUR
  SI (caractereRecherche=="a" OU caractereRecherche=="e" OU caractereRecherche=="i" OU caractereRecherche=="o" OU caractereRecherche=="u" OU caractereRecherche=="y" OU caractereRecherche=="A" OU caractereRecherche=="E" OU caractereRecherche=="I" OU caractereRecherche=="O" OU caractereRecherche=="U" OU caractereRecherche=="Y") ALORS
    DEBUT_SI
    AFFICHER "Résultat : "
    AFFICHER caractereRecherche
    AFFICHER " se retrouve "
    AFFICHER occurences
    AFFICHER " fois, et c’est une voyelle"
    FIN_SI
  SINON
    DEBUT_SINON
    AFFICHER "Résultat : "
    AFFICHER caractereRecherche
    AFFICHER " se retrouve "
    AFFICHER occurences
    AFFICHER " fois, et c’est une consonne"
    FIN_SINON
FIN_ALGORITHME
```

### TP 9
Écrire un algorithme qui demande à l’utilisateur une chaîne de départ, et ensuite l’algorithme devra produire la chaîne renversée.

Exemple :

Si l’on entre : papa

L’algo devra nous afficher : apap

```js
FONCTIONS_UTILISEES
VARIABLES
  str EST_DU_TYPE CHAINE
  size EST_DU_TYPE NOMBRE
  counter EST_DU_TYPE NOMBRE
  reversed EST_DU_TYPE CHAINE
DEBUT_ALGORITHME
  LIRE str
  size PREND_LA_VALEUR str.length
  POUR counter ALLANT_DE 0 A size-1
    DEBUT_POUR
    // counter = 0, reversed="", reversed=str.substr(0,1) + reversed = p+"" = p
    // counter = 1, reversed=p, reversed=str.substr(1,1) + reversed = a + p = ap
    // counter = 2, reversed=ap, reversed=str.substr(2,1) + reversed = p + ap => pap
     // counter =3, reversed=pap, reversed=str.substr(3,1) + reversed = a + pap => apap
    reversed PREND_LA_VALEUR str.substr(counter,1)+reversed
    FIN_POUR
  AFFICHER reversed
FIN_ALGORITHME
```


```js
```js
FONCTIONS_UTILISEES
  FONCTION calculPuissance(n,p)
    VARIABLES_FONCTION
      i EST_DU_TYPE NOMBRE
      resultat EST_DU_TYPE NOMBRE
    DEBUT_FONCTION
    resultat PREND_LA_VALEUR 1
    POUR i ALLANT_DE 1 A p
      DEBUT_POUR
      resultat PREND_LA_VALEUR resultat*n
      FIN_POUR
    RENVOYER resultat
    FIN_FONCTION

  FONCTION reverseString(str)
    VARIABLES_FONCTION
      counter EST_DU_TYPE NOMBRE
      reversed EST_DU_TYPE CHAINE
      size EST_DU_TYPE NOMBRE
    DEBUT_FONCTION
    size PREND_LA_VALEUR str.length
    POUR counter ALLANT_DE 0 A size-1
      DEBUT_POUR
      reversed PREND_LA_VALEUR str.substr(counter,1)+reversed
      FIN_POUR
        AFFICHER reversed
    FIN_FONCTION
VARIABLES
  num EST_DU_TYPE NOMBRE
  power EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  LIRE num
  LIRE power
  AFFICHERCALCUL* calculPuissance(4,2)
  AFFICHERCALCUL* calculPuissance(num,power)
  AFFICHERCALCUL* pow(num,power)
  APPELER_FONCTION reverseString("papa")
FIN_ALGORITHME
```