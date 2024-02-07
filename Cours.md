# COURS

## 1. VARIABLES

### 1.1. Déclaration
```js
FONCTIONS_UTILISEES
VARIABLES
name EST_DU_TYPE CHAINE
age EST_DU_TYPE NOMBRE
ageDeMonPere EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
	name PREND_LA_VALEUR "Christian"
	age PREND_LA_VALEUR 56
	ageDeMonPere PREND_LA_VALEUR 75
	AFFICHER* name
	AFFICHER* age
	AFFICHER* ageDeMonPere
FIN_ALGORITHME
```

### 1.2. Expression
```js
FONCTIONS_UTILISEES
VARIABLES
firstNumber EST_DU_TYPE NOMBRE
secondNumber EST_DU_TYPE NOMBRE
sum EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
firstNumber PREND_LA_VALEUR 5
secondNumber PREND_LA_VALEUR 10
sum PREND_LA_VALEUR firstNumber + secondNumber
AFFICHER firstNumber
AFFICHER " + "
AFFICHER secondNumber
AFFICHER " = "
AFFICHER sum
FIN_ALGORITHME
```

### 1.3. Lecture clavier
```js
FONCTIONS_UTILISEES
VARIABLES
firstNumber EST_DU_TYPE NOMBRE
secondNumber EST_DU_TYPE NOMBRE
sum EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
LIRE firstNumber
LIRE secondNumber
sum PREND_LA_VALEUR firstNumber + secondNumber
AFFICHER firstNumber
AFFICHER " + "
AFFICHER secondNumber
AFFICHER " = "
AFFICHER sum
FIN_ALGORITHME
```

## 2. CONDITIONS

### 2.1. ALTERNATIVES SIMPLES
```js
FONCTIONS_UTILISEES
  //nombre, chaine, liste
VARIABLES
age EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
LIRE age
SI (age>=18) ALORS
	DEBUT_SI
	AFFICHER "Oui, vous pouvez voter."
	FIN_SI
	SINON
		DEBUT_SINON
		AFFICHER "Reviens la prochaine."
		FIN_SINON
FIN_ALGORITHME
```

```js
FONCTIONS_UTILISEES
  //nombre, chaine, liste
VARIABLES
pays EST_DU_TYPE CHAINE
DEBUT_ALGORITHME
LIRE pays
SI (pays=="France" OU pays=="Belgique") ALORS
	DEBUT_SI
	AFFICHER "Vous pouvez participer au sondage."
	FIN_SI
	SINON
		DEBUT_SINON
		AFFICHER "Vous n'êtes pas eligible..."
		FIN_SINON
FIN_ALGORITHME

```

### 2.2. ALTERNATIVES MUTIPLES & CHOIX IMBRIQUES
```js
FONCTIONS_UTILISEES
VARIABLES
  language EST_DU_TYPE CHAINE
DEBUT_ALGORITHME
  LIRE language
  SI (language=="french") ALORS
    DEBUT_SI
    AFFICHER "Salut!"
    FIN_SI
    SINON
      DEBUT_SINON
      SI (language=="english") ALORS
        DEBUT_SI
        AFFICHER "Hello!"
        FIN_SI
        SINON
          DEBUT_SINON
          SI (language=="spanish") ALORS
            DEBUT_SI
            AFFICHER "Hola!"
            FIN_SI
            SINON
              DEBUT_SINON
              SI (language=="german") ALORS
                DEBUT_SI
                AFFICHER "Guten tag!"
                FIN_SI
                SINON
                  DEBUT_SINON
                  AFFICHER "Langue non supportée."
                  FIN_SINON
              FIN_SINON
          FIN_SINON
      FIN_SINON
FIN_ALGORITHME
```

## 3. BOUCLES
```js
FONCTIONS_UTILISEES
VARIABLES
  x EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  // DRY : Don't repeat yourself
  POUR x ALLANT_DE 50 A 100 
    DEBUT_POUR
    AFFICHER "Le carré de "
    AFFICHER x
    AFFICHER " est: "
    AFFICHERCALCUL* pow(x,2)
    FIN_POUR
FIN_ALGORITHME
```

```js
FONCTIONS_UTILISEES
VARIABLES
  chiffre EST_DU_TYPE NOMBRE
  counter EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
  LIRE chiffre
  POUR counter ALLANT_DE 0 A 13 
    DEBUT_POUR
    // 5 x 0 = 0
    // 5 x 1 = 5
    AFFICHER chiffre
    AFFICHER " x "
    AFFICHER counter
    AFFICHER " = "
    AFFICHERCALCUL* chiffre*counter
    FIN_POUR
FIN_ALGORITHME
```

```js
```js
FONCTIONS_UTILISEES
VARIABLES
codePin EST_DU_TYPE NOMBRE 
codePinATester EST_DU_TYPE NOMBRE
nombreTentatives EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
// 1. Ajout du code pin des les reglages de l'appareil
LIRE codePin // 1234

nombreTentatives PREND_LA_VALEUR 3


TANT_QUE (codePinATester!=codePin ET nombreTentatives<=3) FAIRE
	DEBUT_TANT_QUE
  LIRE codePinATester
  nombreTentatives PREND_LA_VALEUR nombreTentatives+1
  SI (codePinATester!=codePin) ALORS 
  	DEBUT_SI
  	AFFICHER "Code Pin invalide. Réecrire"
  	FIN_SI
  	SINON
  		DEBUT_SINON
  		AFFICHER "Bienvenue."
  		FIN_SINON
	FIN_TANT_QUE
FIN_ALGORITHME
```

```js
FONCTIONS_UTILISEES
VARIABLES
name EST_DU_TYPE CHAINE
sub EST_DU_TYPE CHAINE
i EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
LIRE name 
AFFICHERCALCUL* name.length

//[a,b[
// christian
sub PREND_LA_VALEUR name.substr(1,2) 
AFFICHER* sub


POUR i ALLANT_DE 0 A name.length-1
	DEBUT_POUR
	sub PREND_LA_VALEUR name.substr(i,1)
	AFFICHER* sub
	FIN_POUR

FIN_ALGORITHME

```

```js
FONCTIONS_UTILISEES
VARIABLES
name EST_DU_TYPE CHAINE
sub EST_DU_TYPE CHAINE
i EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
// christian
LIRE name
name PREND_LA_VALEUR name+" lisangola"
AFFICHER name
FIN_ALGORITHME
```

```js
FONCTIONS_UTILISEES
VARIABLES
name EST_DU_TYPE CHAINE
a EST_DU_TYPE CHAINE
i EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
// christian
// ASCII
LIRE name
a PREND_LA_VALEUR String.fromCharCode(name.charCodeAt(0))
AFFICHER a

POUR i ALLANT_DE 0 A name.length
	DEBUT_POUR
	a PREND_LA_VALEUR String.fromCharCode(name.charCodeAt(i))
	AFFICHER* a
	FIN_POUR  
FIN_ALGORITHME
```
## 4. TABLEAUX

```js
FONCTIONS_UTILISEES
VARIABLES
notes EST_DU_TYPE LISTE
i EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME

// Sans boucles
notes[0] PREND_LA_VALEUR 12
notes[1] PREND_LA_VALEUR 13
notes[2] PREND_LA_VALEUR 14
notes[3] PREND_LA_VALEUR 9
notes[4] PREND_LA_VALEUR 0

// AFFICHER* notes[0]
// AFFICHER* notes[1]
// AFFICHER* notes[2]
// AFFICHER* notes[3]
// AFFICHER* notes[4]

POUR i ALLANT_DE 0 A 4
    DEBUT_POUR
    AFFICHER* notes[i]
    FIN_POUR  

FIN_ALGORITHME
```

```js
FONCTIONS_UTILISEES
VARIABLES
notes EST_DU_TYPE LISTE
i EST_DU_TYPE NOMBRE
n EST_DU_TYPE NOMBRE
somme EST_DU_TYPE NOMBRE
moyenne EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
AFFICHER "Entrez le nombre de notes que vous souhaitez inserer : "
LIRE n

// [12,13, 14,9,0] 
POUR i ALLANT_DE 0 A n-1
	DEBUT_POUR
	LIRE notes[i]
	FIN_POUR  

somme PREND_LA_VALEUR 0
POUR i ALLANT_DE 0 A n-1
	DEBUT_POUR
	// i = 0, somme = 0, somme = somme + notes[0] => somme = 0 + 12 = 12
	// i = 1, somme = 12, somme = somme + notes[1] => somme = 12 + 13 = 25
	// i = 2, somme = 25, somme = somme + notes[2] => somme = 25 + 14 = 39
	// i = 3, somme = 39, somme = somme + notes[3] => somme = 39 + 9 = 48
	// i = 4, somme = 48, somme = somme + notes[4] => somme = 48 + 0 = 48
	somme PREND_LA_VALEUR somme+notes[i]
	FIN_POUR  	

	// 48/5 => 9,
	moyenne PREND_LA_VALEUR somme/n 

	AFFICHER "Somme : "
	AFFICHER* somme
	AFFICHER "Moyenne : "
	AFFICHER moyenne



FIN_ALGORITHME

```


```js
FONCTIONS_UTILISEES
VARIABLES
notes EST_DU_TYPE LISTE
i EST_DU_TYPE NOMBRE
n EST_DU_TYPE NOMBRE
somme EST_DU_TYPE NOMBRE
moyenne EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME
AFFICHER "Entrez le nombre de notes que vous souhaitez inserer : "
LIRE n

// [12,13, 14,9,0] 
POUR i ALLANT_DE 0 A n-1
	DEBUT_POUR
	LIRE notes[i]
	FIN_POUR  


somme PREND_LA_VALEUR 0
POUR i ALLANT_DE 0 A notes.length	-1
	DEBUT_POUR
	// i = 0, somme = 0, somme = somme + notes[0] => somme = 0 + 12 = 12
	// i = 1, somme = 12, somme = somme + notes[1] => somme = 12 + 13 = 25
	// i = 2, somme = 25, somme = somme + notes[2] => somme = 25 + 14 = 39
	// i = 3, somme = 39, somme = somme + notes[3] => somme = 39 + 9 = 48
	// i = 4, somme = 48, somme = somme + notes[4] => somme = 48 + 0 = 48
	somme PREND_LA_VALEUR somme+notes[i]
	FIN_POUR  	

	// 48/5 => 9,
	moyenne PREND_LA_VALEUR somme/notes.length

	AFFICHER "Somme : "
	AFFICHER* somme
	AFFICHER "Moyenne : "
	AFFICHER moyenne
```

## 5. FONCTIONS


```js
// Avant l'utilisation des fonctions
FONCTIONS_UTILISEES
VARIABLES
n EST_DU_TYPE NOMBRE
puissance EST_DU_TYPE NOMBRE
i EST_DU_TYPE NOMBRE
resultat EST_DU_TYPE NOMBRE
DEBUT_ALGORITHME

n PREND_LA_VALEUR 4
puissance PREND_LA_VALEUR 2

resultat PREND_LA_VALEUR 1 
POUR i ALLANT_DE 1 A puissance
	DEBUT_POUR
	resultat PREND_LA_VALEUR n*n
	FIN_POUR  

AFFICHER resultat

FIN_ALGORITHME

```

