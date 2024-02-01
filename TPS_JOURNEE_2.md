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

