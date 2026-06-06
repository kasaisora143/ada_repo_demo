```text
VARIABLE
	nbHeures : ENTIER
	nbMibutes : ENTIER
	nbSecondes : ENTIER
DEBUT
	nbHeures <- 0
	nbMibutes  <- 0
	nbSecondes <- 0
	AFFICHER "Entrez le nombre d’heures et de minutes"
	LIRE nbHeures
	LIRE nbMibutes
	SI nbHeures < 0 || nbMibutes < 0 ALORS
		AFFICHER "Durée incorrecte."
	SINON
		nbSecondes <- nbHeures * 3600 + nbMinutes * 60
		AFFICHER "Le nombre de secondes correspondant est :
		AFFICHER nbSecondes
	FIN_SI
FIN
```