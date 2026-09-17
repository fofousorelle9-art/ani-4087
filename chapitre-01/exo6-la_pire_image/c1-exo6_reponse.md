Nous allons étudier le temps mis pour effacer l'écran par un code.
A exécution, le code retourne :
- plus longue image : 2.964ms
- Images qui dépassent 11ms : 0

En conclusion, mon code tiendrait dans un casque

Code :
#include <iostream>
#include <chrono>

using namespace std;

int main()
{
    double plusLongue = 0;
    int nombre = 0;
    // Initialisation de la boucle pour 1000 unités
    for (int i = 0; i < 1000; i++)
    {
        auto debut = chrono::steady_clock::now();

        // Effacer l'écran
        cout << "\033[2J\033[H";

        auto fin = chrono::steady_clock::now();
          
        double temps = chrono::duration<double, milli>(fin - debut).count();
         // Calculer l'image la plus longue
        if (temps > plusLongue)
        {
            plusLongue = temps;
        }

        if (temps > 11)
        {
            nombre++;
        }
    }
    cout << "Plus longue image : " << plusLongue << " ms" << endl;
    cout << "Images qui depassent 11 ms : " << nombre << endl;
    return 0;
}
