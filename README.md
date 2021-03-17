#include <stdio.h>

#define NBITS  4 // numero di bit per la codifica FLC
#define NCODES 4 // numero di codici dell'algabeto

// print_code: stampa un simbolo dell'algabeto
//
// Input: simbolo dell'algabeto da stampare
// Output:

void print_code(int code[NBITS]) {
  //inserisci qui il tuo codice
  for(int i = 0; i < NBITS; i++)
    printf("%d", code[i]);
}

// hamming: calcola la distanza di hamming tra due simboli di uno stesso alfabeto
//
// Input: due simboli da confrontare
// Output: distanza di hamming

int hamming(int vet_1[], int vet_2[]) {
    int dist=0;
    for(int i = 0; i < NBITS; i++){
        if(vet_1[i] != vet_2[i])
            dist++;
    }
  //inserisci qui il tuo codice
}

// main: dato un alfabeto, stampa tutte le possibili distanze di hamming tra u sumboli
//       il programma deve stampare la seguente stringa
//       La distanza tra <simbolo 1> e <simbolo 2> = <distanza di hamming>
//
// Input:
// Output:
void main() {
    int codec[NCODES][NBITS] =
    {
        {1, 0, 1, 1},
        {0, 1, 1, 0},
        {1, 0, 0, 1},
        {0, 1, 0, 1},
    };
    // 0-1, 0-2, 0-3,
    // 1-2, 1-3,
    // 2-3

    // i = 0 --> 3
    // i = 1 --> 2
    // i = 2 --> 1
    int distance = hamming(codec[0],codec[1]);
    //inserisci qui il tuo codice
    for (int i = 0; i < NCODES - 1; i++){
        print_code(codec[i]);
        printf("\n");
    }

        //for(int j = i + 1; j <= NCODES -1; j++ ){
                //printf("%d - %d\n", i, j);
                //codec[i], codec[j];

        //printf("la distanza tra %d e %d = %d", codec[i], codec[j], distance );
   }
//}
