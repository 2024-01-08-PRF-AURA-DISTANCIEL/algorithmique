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