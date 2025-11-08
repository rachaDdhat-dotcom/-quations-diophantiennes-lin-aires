<img width="674" height="552" alt="Capture d&#39;écran 2025-11-08 141840" src="https://github.com/user-attachments/assets/16a76779-6325-4a0d-85a2-95c72c3d155c" />




Ce programme résout l’équation diophantienne a*x + b*y = c.
Il commence par calculer le PGCD de a et b à l’aide de l’algorithme d’Euclide, puis applique l’algorithme d’Euclide étendu pour trouver une solution particulière (x0, y0) telle que a*x0 + b*y0 = PGCD(a, b).
Si le PGCD divise c, il existe des solutions entières.
La solution générale s’écrit alors : (x, y) = (xp + α*k, yp + β*k), avec k entier.
