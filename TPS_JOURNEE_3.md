# Exercices

## 1.FONCTIONS

### TP1
Ecrivez une fonction prend en paramètre 2 chaîne dont la première représente un text quelconque et la 2ème un prefix.

Ensuite, faudra que la fonction retourne “VRAI”, si le 2ème paramètre est le préfixe du premier et “FAUX” s’il ne l’est pas.

Exemple :

maFonction("banner", "bang") => retournera FAUX

maFonction(“hugging”,”hug”) =>retournera VRAI

```js
// Solution 1
FONCTIONS_UTILISEES
  FONCTION isPrefix(original, prefix)
    VARIABLES_FONCTION
    i EST_DU_TYPE NOMBRE
    DEBUT_FONCTION
    SI (prefix.length>original.length) ALORS
    	DEBUT_SI
    	RENVOYER 0
    	FIN_SI

    	POUR i ALLANT_DE 0 A prefix.length-1
    		DEBUT_POUR
    		SI (String.fromCharCode(prefix.charCodeAt(i))!=String.fromCharCode(original.charCodeAt(i))) ALORS
    			DEBUT_SI
    			RENVOYER 0
    			FIN_SI
    		FIN_POUR
    		RENVOYER 1
    FIN_FONCTION
VARIABLES
DEBUT_ALGORITHME
AFFICHERCALCUL* isPrefix("papa","papa")
AFFICHERCALCUL* isPrefix("papa","papaya")
AFFICHERCALCUL* isPrefix("banner","bang")
AFFICHERCALCUL* isPrefix("hugging","hug")
FIN_ALGORITHME

```

```js
//Solution 2
FONCTIONS_UTILISEES
// Fonction de comparaison de charactères dans 2 chaines
  FONCTION compareCharsAtPosition(text1,text2, position)
  VARIABLES_FONCTION
  SI (String.fromCharCode(text1.charCodeAt(position))==String.fromCharCode(text2.charCodeAt(position))) ALORS
  	DEBUT_SI
  	RENVOYER 1
  	FIN_SI
  	SINON
  		DEBUT_SINON
  		RENVOYER 0
  		FIN_SINON
  DEBUT_FONCTION
  FIN_FONCTION


  // Notre fonction principale
  FONCTION isPrefix(original, prefix)
    VARIABLES_FONCTION
    i EST_DU_TYPE NOMBRE
    DEBUT_FONCTION
    SI (prefix.length>original.length) ALORS
    	DEBUT_SI
    	RENVOYER 0
    	FIN_SI

    	POUR i ALLANT_DE 0 A prefix.length-1
    		DEBUT_POUR
    		SI (compareCharsAtPosition(original,prefix, i) != 1) ALORS
    			DEBUT_SI
    			RENVOYER 0
    			FIN_SI
    		FIN_POUR
    		RENVOYER 1
    FIN_FONCTION
VARIABLES
DEBUT_ALGORITHME
AFFICHERCALCUL* isPrefix("papa","papa")
AFFICHERCALCUL* isPrefix("papa","papaya")
AFFICHERCALCUL* isPrefix("banner","bang")
AFFICHERCALCUL* isPrefix("hugging","hug")
FIN_ALGORITHME

```

```js
// Solution 3 : Avec substr
FONCTIONS_UTILISEES
  FONCTION isPrefix(original, prefix)
    VARIABLES_FONCTION
    i EST_DU_TYPE NOMBRE
    DEBUT_FONCTION
    SI (prefix.length>original.length) ALORS
    	DEBUT_SI
    	RENVOYER 0
    	FIN_SI
    		SI (original.substr(0,prefix.length)==prefix) ALORS
    			DEBUT_SI
    			RENVOYER 1
    			FIN_SI
    		RENVOYER 0
    FIN_FONCTION
VARIABLES
DEBUT_ALGORITHME
AFFICHERCALCUL* isPrefix("papa","papa")
AFFICHERCALCUL* isPrefix("papa","papaya")
AFFICHERCALCUL* isPrefix("banner","bang")
AFFICHERCALCUL* isPrefix("hugging","hug")
FIN_ALGORITHME
```

## 2. TABLEAUX

### TP 2
Ecrire un algorithme qui demande l’utilisateur de créer 2 listes composées de nombres.

Ensuite, remplir ces 2 listes à partir de la lecture du clavier tout en sachant que ces 2 listes doivent avoir la même taille(aussi définie par une lecture).

Puis, calculer la liste résultante qui va être construite par la somme des éléments de la première liste et avec l’inverse de la 2ème liste.

Exemple :

Liste 1 : [ 2 , 4 , 5 , 7 ,8 ]
Liste 2 : [ 3 , 7 , 2 , 5 , 6 ]
List 3(résultante) : [ 8(2+6) , 9(4+5), 7(5+2) , 14(7+7), 11(8+3) ]

```js
FONCTIONS_UTILISEES
VARIABLES
  liste1 EST_DU_TYPE LISTE
  liste2 EST_DU_TYPE LISTE
  listeRes EST_DU_TYPE LISTE
  i EST_DU_TYPE NOMBRE
  n EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  AFFICHER "Entrez le nombre de notes à ajouter dans la liste."
  LIRE n
  POUR i ALLANT_DE 0 A n-1
    DEBUT_POUR
    // Générer des nombres aléatoires
    // On peut si on veut remplire la résultant directement ici
    liste1[i] PREND_LA_VALEUR floor(random()*20)+1
    liste2[i] PREND_LA_VALEUR floor(random()*20)+1
    FIN_POUR

  // Remplissage de la résultante
  POUR i ALLANT_DE 0 A n-1
    DEBUT_POUR
 			 listeRes[i] PREND_LA_VALEUR liste1[i]+liste2[n-i-1]
    FIN_POUR

  AFFICHER "Liste 1 : "
  POUR i ALLANT_DE 0 A n-1
    DEBUT_POUR
    AFFICHER liste1[i]
    AFFICHER " "
    FIN_POUR
    AFFICHER* " "
  AFFICHER "Liste 1 : "
  POUR i ALLANT_DE 0 A n-1
    DEBUT_POUR
    AFFICHER liste2[i]
    AFFICHER " "
    FIN_POUR
    AFFICHER* " "

      AFFICHER "Résultante : "
     POUR i ALLANT_DE 0 A n-1
    DEBUT_POUR
    AFFICHER listeRes[i]
    AFFICHER " "
    FIN_POUR

FIN_ALGORITHME

```

### TP 3
Ecrire un algorithme qui demande à l’utilisateur d’initialiser un tableau numérique à partir à partir d’un instruction de lecture, et ensuite le plus grand nombre du tableau et le plus petit.

Exemple :

Tableau : [3, 6 , 2 , 1 , 7 , 12 , 32 ]
Plus grand : 32
Plus petit : 1

```js
FONCTIONS_UTILISEES
VARIABLES
  numbers EST_DU_TYPE LISTE
  i EST_DU_TYPE NOMBRE
  n EST_DU_TYPE NOMBRE
  max EST_DU_TYPE NOMBRE
  min EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  AFFICHER "Entrez le nombre de notes à ajouter dans la liste."
  LIRE n
  POUR i ALLANT_DE 0 A n-1
    DEBUT_POUR
    // Générer des nombres aléatoires
    numbers[i] PREND_LA_VALEUR floor(random()*100)+1
    FIN_POUR
  max PREND_LA_VALEUR numbers[0]
  min PREND_LA_VALEUR numbers[0]
  // On pouvait tout gérer dans une seule boucle
  POUR i ALLANT_DE 0 A n-1
    DEBUT_POUR
    SI (numbers[i]>max) ALORS
      DEBUT_SI
      max PREND_LA_VALEUR numbers[i]
      FIN_SI
    SI (numbers[i]<min) ALORS
      DEBUT_SI
      min PREND_LA_VALEUR numbers[i]
      FIN_SI
    FIN_POUR
  AFFICHER "Numbers : "
  POUR i ALLANT_DE 0 A n-1
    DEBUT_POUR
    AFFICHER numbers[i]
    AFFICHER " "
    FIN_POUR
  AFFICHER* " "
  AFFICHER "Max : "
  AFFICHER* max
  AFFICHER "Min : "
  AFFICHER* min
FIN_ALGORITHME
```

### TP 4
Ecrire un algorithme qui demande à l’utilisateur une chaîne de départ, et ensuite l’algorithme devra lui dire si la chaîne saisie est un palindrome ou non.

Se dit d'un mot, d'un vers, d'une phrase que l'on peut lire indifféremment de gauche à droite ou de droite à gauche.

Exemple : le mot ressasser ou la phrase esope reste ici et se repose.

```js
// Solution 1
FONCTIONS_UTILISEES
VARIABLES
  str EST_DU_TYPE CHAINE
  // C'est notre string initial mais sans les espaces
  cleanedStr EST_DU_TYPE CHAINE
  size EST_DU_TYPE NOMBRE
  counter EST_DU_TYPE NOMBRE
  reversed EST_DU_TYPE CHAINE
DEBUT_ALGORITHME
  LIRE str
  size PREND_LA_VALEUR str.length
  POUR counter ALLANT_DE 0 A size-1
    DEBUT_POUR
    SI (String.fromCharCode(str.charCodeAt(counter))!=" ") ALORS
    	DEBUT_SI
    	cleanedStr PREND_LA_VALEUR cleanedStr+str.substr(counter,1)
    	reversed PREND_LA_VALEUR str.substr(counter,1)+reversed
    	FIN_SI
    FIN_POUR
  SI (cleanedStr==reversed) ALORS
  	DEBUT_SI
  	AFFICHER "C'est un palindrome"
  	FIN_SI
  	SINON
  		DEBUT_SINON
  		AFFICHER "Ce n'est pas un palindrome"
  		FIN_SINON
FIN_ALGORITHME
```

```js
// Solution 2
FONCTIONS_UTILISEES
FONCTION isPalindrome(str)
VARIABLES_FONCTION
i EST_DU_TYPE NOMBRE
	DEBUT_FONCTION
	  // On divise la chaine par 2 pour ne pas parcourir toute la chaine, car si on arrive au milieu
	  // Pas besoin de continuer l'iteration
	  POUR i ALLANT_DE 0 A str.length/2
  SI (str.substr(i,1)!=str.substr(str.length-i-1,1)) ALORS
  	DEBUT_SI
  	RENVOYER 0
  	FIN_SI
  	SINON
  		RENVOYER 1
	FIN_FONCTION

VARIABLES
  str EST_DU_TYPE CHAINE
  // C'est notre string initial mais sans les espaces
  cleanedStr EST_DU_TYPE CHAINE
  size EST_DU_TYPE NOMBRE
  counter EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  LIRE str

  // Retirer tous les espaces de la chaine
  size PREND_LA_VALEUR str.length
  POUR counter ALLANT_DE 0 A size-1
    DEBUT_POUR
    SI (String.fromCharCode(str.charCodeAt(counter))!=" ") ALORS
    	DEBUT_SI
    	cleanedStr PREND_LA_VALEUR cleanedStr+str.substr(counter,1)
    	FIN_SI
    FIN_POUR

    AFFICHERCALCUL isPalindrome(cleanedStr)
FIN_ALGORITHME
```

