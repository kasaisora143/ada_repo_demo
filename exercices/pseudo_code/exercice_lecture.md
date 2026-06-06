Soit le pseudo-code suivant :

```
VARIABLE:
      a : ENTIER
      b : ENTIER
      c : ENTIER
DEBUT
	a ← 0
	b ← 0
	c ← 0
	AFFICHER « Entrez trois valeurs entières »
	LIRE a
	LIRE b
	LIRE c
	b ← a
	c ← (a + b) /2
	a ← b + c * 2
	AFFICHER « Le résultat est : »
	AFFICHER a
	SI a == 8 || a >= 3 ALORS
      AFFICHER « Cas n°1 »
	SINON SI a >= 7 ALORS
      AFFICHER "Cas n°2"
  SINON
		  AFFICHER b
	FIN_SI
FIN
```

# Question 1

Exécutez cet algorithme et notez la trace pour les valeurs d’entrée 3, 7 et 12.

Qu’est-ce qui sera affiché par l’algorithme ?