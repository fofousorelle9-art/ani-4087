Le programme efface l'écran, il n'y a donc aucune logique, physique ou chargement des ressiurces. 
En estimant le doublement, le pire cas serait de (2,964 * 2) = 5,928ms, 

En utilisant le budget total des cadences - le double rendu, on aura :
a- 72Hz : 13,9 - 5,928 = 7,972ms
b- 90Hz : 11,1 - 5,928 = 5,172ms
c- 120Hz : 8,3 - 5,928 = 2,372ms

Ainsi, avec ce double rendu, le programme tiendrait dans le budget, même à 120Hz
