```C
#include <ctype.h>
#include <stdio.h>

int calc_pts(char word[]);
int main(void)
{
    char w1[100];
    char w2[100];

    // Input from user

    printf("Player 1: ");
    scanf("%s", w1);
    printf("Player 2: ");
    scanf("%s", w2);

    int p1 = calc_pts(w1);
    int p2 = calc_pts(w2);

    // check who won
    if (p1 > p2)
    {
        printf("Player 1 wins!");
    }
    else if (p2 > p1)
    {
        printf("Player 2 wins!");
    }
    else
    {
        printf("Tie!");
    }
    return 0;
}

int calc_pts(char word[])
{
    int points = 0;
    // Points per letter:
    int A = 1, B = 3, C = 3, D = 2, E = 1, F = 4, G = 2, H = 4, I = 1, J = 8, K = 5, L = 1, M = 3,
        N = 1, O = 1, P = 3, Q = 10, R = 1, S = 1, T = 1, U = 1, V = 4, W = 4, X = 8, Y = 4, Z = 10;

    for (int i = 0; word[i] != '\0'; i++)
    {
        char uppercase = toupper(word[i]);
        if (uppercase >= 'A' && uppercase <= 'Z')
        {
            switch (uppercase)
            {
                case 'A':
                    points += A;
                    break;
                case 'B':
                    points += B;
                    break;
                case 'C':
                    points += C;
                    break;
                case 'D':
                    points += D;
                    break;
                case 'E':
                    points += E;
                    break;
                case 'F':
                    points += F;
                    break;
                case 'G':
                    points += G;
                    break;
                case 'H':
                    points += H;
                    break;
                case 'I':
                    points += I;
                    break;
                case 'J':
                    points += J;
                    break;
                case 'K':
                    points += K;
                    break;
                case 'L':
                    points += L;
                    break;
                case 'M':
                    points += M;
                    break;
                case 'N':
                    points += N;
                    break;
                case 'O':
                    points += O;
                    break;
                case 'P':
                    points += P;
                    break;
                case 'Q':
                    points += Q;
                    break;
                case 'R':
                    points += R;
                    break;
                case 'S':
                    points += S;
                    break;
                case 'T':
                    points += T;
                    break;
                case 'U':
                    points += U;
                    break;
                case 'V':
                    points += V;
                    break;
                case 'W':
                    points += W;
                    break;
                case 'X':
                    points += X;
                    break;
                case 'Y':
                    points += Y;
                    break;
                case 'Z':
                    points += Z;
                    break;
            }
        }
    }

    return points;
}
```
