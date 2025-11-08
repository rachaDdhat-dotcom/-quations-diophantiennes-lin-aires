<img width="674" height="552" alt="Capture d&#39;écran 2025-11-08 141840" src="https://github.com/user-attachments/assets/16a76779-6325-4a0d-85a2-95c72c3d155c" />
Ce programme résout l’équation diophantienne ( a x + b y = c ).
Il commence par calculer le **PGCD** de ( a ) et ( b ) à l’aide de l’algorithme d’Euclide, puis utilise l’**algorithme d’Euclide étendu** pour trouver une solution particulière ((x_0, y_0)) telle que ( a x_0 + b y_0 = \text{PGCD}(a,b) ).
Si le PGCD divise ( c ), il existe des solutions entières, et la solution générale s’écrit
((x, y) = (x_p + \alpha k, y_p + \beta k)), avec (k \in \mathbb{Z}).
