# Menu-tortas
Imprimir el menú de tortas desde un archivo.
#include <stdio.h>
#include <stdlib.h>
int main (int argc, char** argv)
{
    char num[10];
    char tortas[30];
    char tipo[30];
    char precio[10];
    FILE *tort;
    tort= fopen("tortas.txt", "r");
    fscanf(tort, "%s%s%s%s", num, tortas, tipo, precio);
    while(!feof(tort))
    {
    printf("%s %s %s %s\n", num, tortas, tipo, precio);
    fscanf(tort, "%s%s%s%s", num, tortas, tipo, precio);
    }
    printf("%s %s %s\n", num, tortas, tipo );
    system("pause");
    return 0;
}
