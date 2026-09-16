Nous allons calculer la durée d'une image : 
a- La durée d'une image à 72 hertz, durée = (1000 / 72) = 13,888 sensiblement égal à 13,89ms
b- La durée d'une image à 90 hertz, durée = (1000 / 90) = 11,111 sensiblement égal à 11,11ms
c- La durée d'une image à 120 hertz, durée = (1000 / 120) = 8,333 sensiblement égal à  8,33ms 


Ensuite, nous allons retirer les 8ms qui seront utilisés pour les capteurs, la transmission, la composition, on a :
a- 72 Hz : 13,89 - 8 = 5,89ms
b- 90 Hz : 11,11 - 8 = 3,11ms
c- 120 Hz : 8,33 - 8 = 0,33ms

En conclusion, nous observons que plus la fréquence augmente, plus le temps d'éxécution du code diminue.
