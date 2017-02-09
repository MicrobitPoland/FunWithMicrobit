# Animacje

## Czego nauczysz si� w tym rozdziale?

* Wy�wietla� tekst na swoim BBC Micro:bicie
* Wy�wietla� obrazki na swoim BBC Micro:bicie
* ��czy� tekst z obrazkami

## Wy�wietlanie obraz�w

Wy�wietlanie tekstu jest fajne, ale spr�bujmy teraz powy�wietla� obrazki!

Zacznijmy z czym�...weso�ym:)

```python
from microbit import *

display.show(Image.HAPPY)
```

Czy przes�a�e� kod do swojego Micro:bita?


To jest lista obrazk�w, kt�re mo�esz u�y�:

```python
Image.HEART
Image.HEART_SMALL
Image.HAPPY
Image.SMILE
Image.SAD
Image.CONFUSED
Image.ANGRY
Image.ASLEEP
Image.SURPRISED
Image.ROLLERSKATE
Image.DUCK
Image.HOUSE
Image.TORTOISE
Image.BUTTERFLY
Image.STICKFIGURE
Image.GHOST
Image.SWORD
Image.GIRAFFE
Image.SKULL
Image.UMBRELLA
Image.SNAKE
```

Spr�buj wypr�bowa� kilka z nich.

Spr�buj r�wnie� wy�wietli� wi�cej ni� jeden obrazek!

```python
from microbit import *

display.show(Image.HAPPY)
display.show(Image.HOUSE)
```

Podyskutujmy teraz o rezultacie tego kodu:)

# Wy�wietlanie 2 obrazk�w

Nie widzimy pierwszego obrazka, poniewa�...Micro:bit wykonuje wy�wietlenie drugiego obrazka tak szybko, �e nie widzimy tego pierwszego.

Popro�my Micro:bita, �eby na troch�...zasn��.

Jest specjalna komenda, kt�ra nazywa si� sleep(seconds*1000), kt�ra przenosi Twojego Micro:bita w specjalny rodzaj snu.

Spr�bujmy wpisa� t� komend�, a wewn�trz ,,(seconds*1000)" powiniene� zast�pi� s�owo ,,seconds" liczb� sekund, w czasie kt�rych chcesz, �eby Tw�j Micro:bit spa�.

```python
from microbit import *

display.show(Image.HAPPY)
sleep(10*1000)
display.show(Image.HOUSE)
```

Wy�wietl ten kod i zobacz jak dzia�a!

# Stw�rz sw�j w�asny obrazek!

Micro:bit zna wiele r�nych obrazk�w, ale mo�emy te� stworzy� nowe.

To dzia�a tak:


```python
new_image = Image(
             "11111:"
             "19991:"
             "19991:"
             "19991:"
             "11111")
display.show(new_image)
```
W�a�nie stworzyli�my nowy obrazek!

Ale czym s� te numery?

Mamy 5 linijek i 5 numer�w w ka�dej linijce.

To s� nasze diody! 

Ka�dy numer oznacza jedn� diod� na naszym Micro:bicie, pocz�wszy od lewego g�rnego rogu.

Mamy tutaj 1 i 9.

Czy mo�esz powiedzie� co si� zmienia, jak u�ywamy 0, 1 lub 9 ?

Wskaz�wka: mo�emy tu u�ywa� numer�w od 0 do 9.

Poeksperymentuj!
