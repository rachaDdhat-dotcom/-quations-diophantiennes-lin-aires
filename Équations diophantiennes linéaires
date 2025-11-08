#include <stdio.h>
#include <stdlib.h>

// 1. Algorithme d’Euclide : calcul du PGCD
int pgcd(int a, int b) {
    int temp;
    while (b != 0) {
        temp = b;
        b = a % b;
        a = temp;
    }
    return (a < 0) ? -a : a; // pour gérer les entiers négatifs
}

// 2. Algorithme d’Euclide étendu
// Retourne d = pgcd(a, b) et modifie x et y tels que a*x + b*y = d
int euclide_etendu(int a, int b, int *x, int *y) {
    if (b == 0) {
        *x = 1;
        *y = 0;
        return a;
    } else {
        int x1, y1;
        int d = euclide_etendu(b, a % b, &x1, &y1);
        *x = y1;
        *y = x1 - (a / b) * y1;
        return d;
    }
}

// 3. Programme principal
int main() {
    int a, b, c;
    int d, x0, y0;
    int xp, yp;
    int alpha, beta;

    printf(" Résolution de l’équation diophantienne ax + by = c\n");
    printf("Entrez la valeur de a : ");
    scanf("%d", &a);
    printf("Entrez la valeur de b : ");
    scanf("%d", &b);
    printf("Entrez la valeur de c : ");
    scanf("%d", &c);

    printf("\nRésolution de l’équation : %d x + %d y = %d\n\n", a, b, c);

    // Étape 1 : PGCD et coefficients de Bézout
    d = euclide_etendu(a, b, &x0, &y0);

    printf("Étape 1 — PGCD et coefficients de Bézout :\n");
    printf("pgcd(%d, %d) = %d\n", a, b, d);
    printf("x0 = %d, y0 = %d → %d*%d + %d*%d = %d\n\n", 
           x0, y0, a, x0, b, y0, a*x0 + b*y0);

    // Étape 2 : Vérification d’existence
    if (c % d != 0) {
        printf("Pas de solution entière car %d ne divise pas %d.\n", d, c);
        return 0;
    }

    printf("il existe des solutions entières car %d divise %d.\n\n", d, c);

    // Étape 3 : Calcul d’une solution particulière
    int k = c / d;
    xp = x0 * k;
    yp = y0 * k;

    printf("Étape 2 — Une solution particulière :\n");
    printf("xp = %d, yp = %d\n", xp, yp);
    printf("Vérification : %d*%d + %d*%d = %d\n\n", a, xp, b, yp, a*xp + b*yp);

    // Étape 4 : Forme générale des solutions
    alpha = b / d;
    beta = -a / d;

    printf("Étape 3 — Famille de toutes les solutions :\n");
    printf("(x, y) = (%d + %d*k, %d + %d*k),  k ∈ ℤ\n", xp, alpha, yp, beta);
    printf("Où : α = %d, β = %d, d = %d\n", alpha, beta, d);

    return 0;
}
