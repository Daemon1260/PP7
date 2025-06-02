# Aufgabe 1 – C-Kompilierungsphasen

## sample.c

```c
#include <stdio.h>

int main(void) {
    printf("Hello, PP7!\n");
    return 0;
}

Kompilierungsschritte
1. Präprozessor:
	gcc -E sample.c -o sample.i
	Erzeugt sample.i mit expandierten Includes und Makros.

2. Kompilierung zu Assembler:
	gcc -S sample.i -o sample.s
	Erzeugt sample.s mit Assembly-Code.

3. Assemblierung:
	gcc -c sample.s -o sample.o
	Erzeugt sample.o als Objektdatei.

4.Verlinkung:
	gcc sample.o -o sample
	Erzeugt ausführbare Datei sample.

Ergebnis:

./sample

Hello,PP7
