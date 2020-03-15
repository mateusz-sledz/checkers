# Dokumentacja projektu - Warcaby
Przedmiot: PSZT

Autorzy: Mateusz Śledź, Kacper Zając


Treść zadania:
Wykorzystując algorytm min-max i odcinanie alfa-beta zaprojektować i zaimplementować algorytm umożliwiający rozegranie gry w Warcaby. Działanie algorytmu należy zaprezentować w formie prostej interaktywnej aplikacji graficznej/konsolowej umożliwiającej rozegranie gry zgodnie z jej regułami przeciwko komputerowi. 

WE: kto rozpoczyna grę, maksymalna głębokość przeszukiwania przestrzeni stanów.
WY: prosty interfejs gry.


Założenia:
1. Zamiana pionka w damkę po dojściu do przeciwnej strony planszy.
2. Nakaz bicia.
3. Możliwe wielokrotne bicia.


Algorytm.

Program umożliwia rozegranie gry w warcaby przeciwko komputerowi, wykorzystując zaimplementowany algorytm min-max z odcinaniem alfa-beta. Użytkownik jest graczem szukającym maksimum, a komputer szukającym minimum.
Algorytm rozpoczyna działanie od wygenerowania drzewa gry. W korzeniu drzewa jest zapisana aktualna plansza. Następnie od korzenia rozchodzą się węzły zawierające plansze gry jeden ruch do przodu, a od nich kolejne plansze będące rozwinięciem węzła rodzica o jeden ruch. W zależności od parametru depth tworzone jest drzewo o podanej wysokości.
Narzędziem podejmowania decyzji przez program jest funkcja oceniająca stan gry na podstawie planszy. Funkcja ta rozróżnia pionki przeciwnych drużyn oraz „damki”. Wynikiem funkcji oceniającej jest suma punktów przyznanych za figury obu graczy, przy czym punkty komputera są liczone ujemnie.
Po wygenerowaniu drzewa gry, program wywołuje algorytm minimax, który na podstawie wartości oceny liści drzewa gry wybiera najkorzystniejszy ruch z punktu widzenia komputera. Algorytm korzysta z obcinania alfa-beta, to znaczy wykrywa oraz redukuje poddrzewa, które nic nie zmienią w końcowym wyborze ruchu.
