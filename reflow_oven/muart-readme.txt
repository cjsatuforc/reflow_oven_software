Biblioteka "muart"
Opis: Biblioteka s�u�y do obs�ugi sprz�towego UART w procesorach ATMEGA8 oraz ATMEGA48/88/168/328.

U�ycie: 

1. Skopiuj pliki "muart.h" oraz "muart.c" do katalogu projektu.
2. Wyedytuj plik Makefile (je�li jest taka potrzeba).
3. W nag��wkach projektu dodaj #include "muart.h"
4. W muart.h zdefiniuj odpowiednio RS_BAUD (linia 9)
5. U�yj funkcji inicjalizacyjnej : uart_init();
6. U�ywaj funkcji z biblioteki:

void uart_init(void);
/*
Inicjalizuje UART. U�yj jednorazowo przed korzystaniem z transmisji.
*/

void uart_putc(uint8_t data);
/*
Wysy�a pojedy�czy znak 1-bajtowy
*/

void uart_puts(const char *s );
/*
Wysy�a ci�g znak�w, na przyk�ad napis:
uart_puts("NAPIS");
*/

uint8_t uart_ischar(void);
/*
Sprawdza, czy w buforze s� odebrane dane; funkcja wewn�trzna

*/

uint8_t uart_getc(void);
/*
Odbiera znak 1-bajtowy
*/