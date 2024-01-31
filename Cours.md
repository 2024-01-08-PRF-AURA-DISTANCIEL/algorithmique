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
