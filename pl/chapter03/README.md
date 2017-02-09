# Hello Micro:bit

## Czeg nauczysz si� w tym rozdziale?

* Pokazywa� tekst na swoim Micro:bicie
* P�tli

## Jak poprosi� swojego Micro:bita, �eby powiedzia� ,,Hello!"

Tw�j Micro:bit mo�e robi� wiele r�znych rzeczy, ale musisz mu wytlumaczy�, jak ma je robi�.
To tak jakby� co� czyta�, uczy� si�, i musia� ,,zaimportowa�" to, co przeczyta�e� do m�zgu.

A teraz czas, by otworzy� **MuEditor** i wpisa� kilka pierwszych linijek kodu:

```python
# This is a COMMENT
from microbit import display
```

STOP !

Pomy�lmy o 2 pierwszych linijkach.
Pierwsza linijka zaczyna si� znakiem # i oznacza, �e to, co jest za tym znakiem, jest komentarzem.
Komentarz jest ,,niewidoczn�" dla komputera cz�ci� kodu, kt�ra jest przydatna tylko dla cz�owieka, bo tylko on j� widzi. Komentarz to taka notatka dla nas, albo dla innych ludzi, opisuj�ca co dzieje si� w danym fragmencie kodu.

Kolejna linijka jest ju� du�o wa�niejsza. Prosimy w niej Pythona, �eby zimportowa� nam modu� __display__ z modu�u microbit.

Czym jest modu�?
Pomy�lmy o nim jako pewnym konkretnym fragmencie kodu Pythona, napisanym ju� wcze�niej przez tw�rc�w j�zyka Python, kt�ry mo�emy �ci�gn�� (zaimportowa�), i kt�ry pomaga nam w naszej dalszej pracy. 
Czyli kto� kiedy� napisa� pewne komendy w Pythonie, kt�rymi mo�emy teraz pos�ugiwa� si� by nasza zabawa z programowaniem by�a �atwiejsza.

Teraz mo�emy poprosi� Micro:bita, by wy�wietli� nam poni�szy tekst:

```python
# To jest ZN�W komentarz, mogliby�my tu wpisa� jak�� notatk�, albo cokolwiek innego, to widzi tylko cz�owiek
from microbit import display

display.show("Hello WpiszSwojeImie, I am your Micro:bit")
```

Co tym razem tutaj si� dzieje?

Pierwsza i druga linijka nie s� niczym nowym.

A o co chodzi w trzeciej linijce kodu?

U�ywamy fragmentu kodu, kt�rym jest s�owo _show_ wyst�puj�ce wewn�trz kodu, fragemntu kodu, jakim jest s�owo _display_.

Display po angielsku oznacza: wy�wietl, lub te� wy�wietlacz, a s�owo show = poka�.

Spr�bujmy teraz napisa� podobny kod, ale z innym tekstem:

```python

from microbit import display

display.show("Helloo Poland!)
```

Skopiuj ten tekst do swojego edytora Mu i naci�nij Flash!

Mmmm.... czemu otrzymujemy Error, czyli b��d?

* Wykrzyknik na ko�cu zdania powoduje problem?
* Tekst jest za kr�tki?
* Potrzebujemy znaku " na ko�cu tekstu?
* Helloo (po angielsku powinno by� ,,Hello") nie jest zapisane poprawnie?

## Ale czemu robi� to tylko jeden raz?

W naszym kodzie przes�ali�my Micro:bitowi tekt, kt�ry ma wy�wietla�. Micro:bit wy�wietla ten tekst tylko raz.
Co zrobi�, je�li chceby, by nasz Micro:bit wy�wietla� nasz tekst ca�y czas?
Musimy przedstawi� Wam koncepcj� p�tli (p�tla po angielsku to ,,loop").

Za pomoc� ,,p�tli" m�wimy Micro:bitowi, �eby robi� co� dop�ki jaki� warunek jest spe�niony.

W Pythonie mamy r�ne rodzaje p�tli (czyli r�ne loops). Teraz zaczniemy u�ywa� jednej z tych p�tli. P�tla ta nazywa si�: while.

Komenda ,,while" jest komunikatem, kt�ry brzmi dok�adnie tak: r�b co�, dop�ki warunek, czy te� inaczej nasze za�o�enia s� prawdziwe.

```python
from microbit import display

while 1>0:
  display.show("Hello Poland!")
```

Teraz spr�bujmy w takim kodem:

```python
from microbit import display

while 1<0:
  display.show("Hello Poland!")
```

W�a�nie zmienili�my warunek na co�, co jest zawsze nieprawdziwe.

## Jaka jest r�nica mi�dzy tymi dwoma fragmentami kodu?

## Czemu komenda ,,display" nie jest napisana tu� pod s�owem ,,while"?
