# Przyciski & Sensory

## Czego nauczysz si� w tym rozdziale?

* U�ywania przycisk�w w celu kontrolowania Twojego Micro:bita
* Pokazywania obrazk�w na Twoim Micro:bicie
* ��czenia teksu i obrazk�w

## Mamy przyciski

Jak ju� pewnie zauwa�y�e�, Micro:bit ma 2 du�e przyciski: A i B.
Mo�esz nimi zrobi� wiele ciekawych rzeczy. Zacznijmy od czego� prostego.


```python
from microbit import *

sleep(10 * 1000)
display.scroll(str(button_a.get_presses()))
```

Poczekaj chwil� przed wy�wietleniem kodu!

Wiemy ju� mniej wi�cej, co oznacza: ,,from microbit import *". (microbit to modu�, gwiazdka oznacza ,,wszystko", czyli wszystkie modu�y dost�pne do u�ycia w microbicie). Wiemy te�, co oznacza: `sleep(10 * 1000)`.

A co znaczy ten fragment: ,,display.scroll(str(button_a.get_presses()))"?

Widzimy, �e ta linijka sk�ada si� z kilku r�nych pojedynczych instrukcji.

Od �rodka mamy:

1. `button_a.get_presses()`

Ten kod zwraca nam liczb� klikni�� przycisku A.

2. `str()`

Ta linijka zamienia ,,value", czyli otrzyman� liczb�, na string.
String jest jednym z rodzaj�w danych, jakie rozumie Python (obok np. liczb). Jest to po prostu fragment znak�w, liter, czy wyraz, w odr�nieniu od na przyk�ad liczby.(Liczby mo�na np. dodawa�, a string�w ju� nie, bo to inny typ danych).
"1" i 1 to r�ne warto�ci w Pythonie.  "1" (zapisane w cudzys�owiu) to jest string (czyli wyraz), natomiast 1 to jest liczba, w tym wypadku liczba ca�kowita, czyli po angielsku integer.
Musimy zamieni� liczb� na string, poniewa� komenda ,,dispal.scroll()" rozumie tylko stringi.

3. `display.scroll()`

Tej komendy wcze�niej ju� u�yli�my. Wy�wietla ona wskazany tekst za po�rednictwem diod.

Podsumowuj�c wszystko razem:

1. Zbieramy ilo�� klikni�� przycisku A
2. Zmieniamy ten numer na string
3. Wy�wietlamy warto�� na Micro:bicie

Ok, teraz mo�esz klikn�� Flash, by wy�wietli� sw�j kod!

### Jak dzia�a ten kod?
### Jak my�lisz, jak mo�emy poprawi� ten kod?

### Zadanie

Czy umiesz napisa� program, kt�ry liczy liczb� klikni�� przycisku B w ci�gu 5 sekund?

Masz 10 minut!

## Czas na ulepszenie kodu: cz�� 1#

Ten kod dzia�a, ale chcieliby�my te� doda� kilka nowych funkcjonalno�ci:

Chcemy, by przed rozpocz�ciem liczenia wy�wietla�o si� odliczanie, np. 3, 2, 1, 0, start! Czyli w skr�cie:

* poka� odliczanie (np. 3, 2, 1, 0)
* poka� liczb� klikni�� przycisku B
 
```python
from microbit import *

countdown = ['3','2','1','0']
display.show(countdown, 1*1000)
display.clear() # T� linijk� ,,czy�cimy" nasz wy�wietlacz :)

sleep(10 * 1000)
display.scroll(str(button_b.get_presses()))
```

## Czas na ulepszenie naszego kodu: cz�� 2#

Teraz chcemy jeszcze doda� tekst przed odliczaniem: ,,Naci�nij przycisk A �eby zacz��"

Innymi s�owy chcemy, �eby Micro:bit wy�wietla� nam informacj�, �e mamy nacisn�� przycisk A, o ile nie jest ju� wci�ni�ty.

Jak mo�emy to zakodowa�?

```python
from microbit import *

while button_a.was_pressed() is False:
    display.scroll("Press button A to start")

countdown = ['3','2','1','0']
display.show(countdown, 1*1000)
display.clear()

sleep(10 * 1000)
display.scroll(str(button_b.get_presses()))
```


## Ostatni krok!

Ostatnim krokiem b�dzie mo�liwo�� powt�rzenia gry.

To oznacza niesko�czone powtrzanie kodu, kt�ry napisali�my wcze�niej.

wskaz�wka: �eby powtarza� kod w niesko�czono�� musimy u�y� komendy ,,while True" (czyli: dop�ki prawda, zr�b co�)

```python
from microbit import *

while True:
    while button_a.was_pressed() is False:
        display.scroll("Press button A to start")
        
    countdown = ['3','2','1','0']
    display.show(countdown, 1*1000)
    display.clear()
    sleep(10 * 1000)
    display.scroll(str(button_b.get_presses()))
```

## Poczuj sensory

Micro:bit ma r�zne sensory. Jednym z nich jest akcelerometr, kt�rego mo�emy u�y� do rozpoznawania niekt�rych ruch�w.

```python
up
down
left
right
face up
face down
freefall
3g
6g
8g
```

Mo�esz otrzyma� aktualne po�o�enie Micro:bita u�ywaj�c komendy: ,,accelerometer.current_gesture()". Ta komenda w wyniku zwr�ci nam string.

Spr�bujmy to zobaczy� na prostym przyk�adzie:

```python
from microbit import *


x = Image("90009:"
          "09090:"
          "00900:"
          "09090:"
          "90009")

square = Image("99999:"
               "99999:"
               "99999:"
               "99999:"
               "99999")

while True: 
    gesture = accelerometer.current_gesture()
    if gesture == "face up":
        display.show(square)
    else:
        display.show(x)
```

Wy�wietl ten kod!
