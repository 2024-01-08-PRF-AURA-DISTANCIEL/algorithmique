# Exercices

## 1.VARIABLES

### TP1

```js
A = 5 

B = A

A = 9

B = 5 # Reponse
```

### TP2

```bash
A = 5

B = 7

C = (A + B)/2

A = 12

B = 12

C = 6 # Reponse
```

### TP3

Ecrire un algorithme qui demande à l’utilisateur d’entrer à partir du clavier:

- La distance parcours(m)
- Le temps(sec)

Puis calculer la vitesse selon la formule:

`vitesse = distance parcourue / temps`

Puis afficher le résultat dans le format suivant : `345 m/s`

```js
FONCTIONS_UTILISEES
VARIABLES
  distance EST_DU_TYPE NOMBRE
  temps EST_DU_TYPE NOMBRE
  vitesse EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  LIRE distance
  LIRE temps
  vitesse PREND_LA_VALEUR distance/temps
  AFFICHER vitesse
  AFFICHER "m/s"
FIN_ALGORITHME
```

## 2.CONDITIONS

### TP4
Écrire un algorithme qui demande à l'utilisateur trois notes, puis affiche la moyenne de ces notes. Cependant, si la moyenne est inférieure à 10, le programme doit afficher "Recalé", sinon, il affiche "Admis".

```js
FONCTIONS_UTILISEES
VARIABLES
  n1 EST_DU_TYPE NOMBRE
  n2 EST_DU_TYPE NOMBRE
  n3 EST_DU_TYPE NOMBRE
  somme EST_DU_TYPE NOMBRE
  moyenne EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  LIRE n1
  LIRE n2
  LIRE n3
  somme PREND_LA_VALEUR n1+n2+n3
  moyenne PREND_LA_VALEUR somme/3
  SI (moyenne>=10) ALORS
    DEBUT_SI
    AFFICHER "Admis"
    FIN_SI
    SINON
      DEBUT_SINON
      AFFICHER "Recale"
      FIN_SINON
FIN_ALGORITHME
```

### TP5
Écrire un algorithme qui demande à l'utilisateur de saisir un jour de la semaine. Si c'est un jour ouvré (du lundi au vendredi), le programme affiche "Travail", sinon, s'il s'agit d'un week-end (samedi ou dimanche), il affiche "Repos".

```js
// V1
FONCTIONS_UTILISEES
VARIABLES
  jour EST_DU_TYPE CHAINE
DEBUT_ALGORITHME
  LIRE jour
  SI (jour=="samedi" OU jour=="dimanche") ALORS
    DEBUT_SI
    AFFICHER "Repos"
    FIN_SI
    SINON
      DEBUT_SINON
      AFFICHER "Travail"
      FIN_SINON
FIN_ALGORITHME
```
```js
//V2

```js
FONCTIONS_UTILISEES
VARIABLES
jourDeLaSemaine EST_DU_TYPE CHAINE
DEBUT_ALGORITHME
lire jourDeLaSemaine
SI (jourDeLaSemaine != "lundi" ET jourDeLaSemaine != "mardi" ET jourDeLaSemaine != "mercredi" ET jourDeLaSemaine != "jeudi" ET jourDeLaSemaine != "vendredi" ET jourDeLaSemaine !="samedi" ET jourDeLaSemaine!="dimanche") ALORS
  DEBUT_SI
  AFFICHER "Saisie invalide"
  FIN_SI
  SINON
    DEBUT_SINON
    SI (jourDeLaSemaine=="samedi" OU jourDeLaSemaine=="dimanche") ALORS
      DEBUT_SI
      AFFICHER "Weekend"
      FIN_SI
      SINON
        DEBUT_SINON
        AFFICHER "Travail."
        FIN_SINON
    FIN_SINON
FIN_ALGORITHME

```

### TP6
Écrire un algorithme qui demande l’âge d’un enfant. Ensuite, il l’informe de sa catégorie :

« Poussin » de 7 à 9 ans

« Pupille » de 10 à 11 ans

« Benjamin » de 12 à 13 ans

« Minime » de 14 à 15 ans

« Cadet » 16 à 17 ans

```js
FONCTIONS_UTILISEES

VARIABLES
age EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
	LIRE age
	SI (age>=7 ET age<=9) ALORS
		DEBUT_SI
		AFFICHER* "«Poussin» de 7 à 9 ans."
		FIN_SI
		SINON
			DEBUT_SINON
		SI (age>=10 ET age<=11) ALORS
			DEBUT_SI
			AFFICHER* "«Pupille» de 10 à 11 ans."
			FIN_SI
			SINON
			DEBUT_SINON
			SI (age>=12 ET age<=13) ALORS
				DEBUT_SI
				AFFICHER* "«Benjamin» de 12 à 13 ans."
				FIN_SI
				SINON
				DEBUT_SINON
				SI (age>=14 ET age<=15) ALORS
					DEBUT_SI
					AFFICHER* "«Minime» de 14 à 15 ans."
					FIN_SI
					SINON
					DEBUT_SINON
					SI (age>=16 ET age<=17) ALORS
						DEBUT_SI
						AFFICHER* "«Cadet» 16 à 17 ans."
						FIN_SI
						SINON
							DEBUT_SINON
							AFFICHER* "Catégorie ivalide."
							FIN_SINON
						FIN_SINON
					FIN_SINON
				FIN_SINON
			FIN_SINON
FIN_ALGORITHME
```

### TP7
Écrire un algorithme pour un service de livraison. Le programme demande à l'utilisateur de saisir le poids d'un colis et la distance à parcourir pour la livraison. Si le poids est inférieur à 5 kg et la distance est inférieure à 10 km, le coût de livraison est de 5 euros. Sinon, le coût est de 10 euros.

```js
FONCTIONS_UTILISEES
VARIABLES
  poids EST_DU_TYPE NOMBRE
  distance EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  LIRE poids
  LIRE distance
  SI (poids<5 && distance < 10) ALORS
    DEBUT_SI
    AFFICHER "Le cout est 5 euros"
    FIN_SI
    SINON
      DEBUT_SINON
      AFFICHER "Le cout est de 10 euros"
      FIN_SINON
FIN_ALGORITHME

```

### TP8
Écrivez un programme Java qui permet de résoudre une équation du 2nd degré de la forme ax2+bx+c = 0.
L’utilisateur devra fournir a,b,c à partir du clavier, ensuite le programme lui donnera la solution
Principe du fonctionnement d’une équation du 2nd degré:

https://www.maths-et-tiques.fr/telech/Secondegre2ESL.pdf

```js
FONCTIONS_UTILISEES
VARIABLES
  a EST_DU_TYPE NOMBRE
  b EST_DU_TYPE NOMBRE
  c EST_DU_TYPE NOMBRE
  delta EST_DU_TYPE NOMBRE
  x1 EST_DU_TYPE NOMBRE
  x2 EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  LIRE a
  LIRE b
  LIRE c
  SI (a==0) ALORS
    DEBUT_SI
    AFFICHER "a est nul, donc ce n'est pas une équation du second degré."
    FIN_SI
    SINON
      DEBUT_SINON
      delta PREND_LA_VALEUR pow(b,2)-4*a*c
      SI (delta>=0) ALORS
        DEBUT_SI
        x1 PREND_LA_VALEUR (-b-sqrt(delta))/(2*a)
        x2 PREND_LA_VALEUR (-b+sqrt(delta))/(2*a)
        SI (delta==0) ALORS
          DEBUT_SI
          AFFICHER* "L'équation admet une seule racine x1 = x2"
          FIN_SI
        AFFICHER "x1 : "
        AFFICHER* x1
        AFFICHER "x2 :"
        AFFICHER x2
        FIN_SI
        SINON
          DEBUT_SINON
          AFFICHER* "L'équation n'admet aucune racine réelle."
          FIN_SINON
      FIN_SINON
FIN_ALGORITHME
```

### TP9
Ecrire un programme Java qui déclare 3 variables, a,b,c et qui va ensuite effectuer une permutation de ces valeurs :
Exemple :
Entrez la première valeur(a) : 51
Entrez la deuxième valeur(b) : 876
Entrez la troisième valeur(c) : 235
Les valeurs entrées sont : a = 51, b = 876 et c = 235
Permutation: b <== a, c <== b, a <== c
Les valeurs permutées sont : a = 235, b = 51 et c = 876

```js
FONCTIONS_UTILISEES
VARIABLES
  a EST_DU_TYPE NOMBRE
  b EST_DU_TYPE NOMBRE
  c EST_DU_TYPE NOMBRE
  temp EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  LIRE a
  LIRE b
  LIRE c
  AFFICHER "Avant permutation : a = "
  AFFICHER a
  AFFICHER ", b = "
  AFFICHER b
  AFFICHER ", c ="
  AFFICHER* c
  temp PREND_LA_VALEUR a
  a PREND_LA_VALEUR c
  c PREND_LA_VALEUR b
  b PREND_LA_VALEUR temp
  AFFICHER "Après permutation : a = "
  AFFICHER a
  AFFICHER ", b = "
  AFFICHER b
  AFFICHER ", c ="
  AFFICHER c
FIN_ALGORITHME
```

