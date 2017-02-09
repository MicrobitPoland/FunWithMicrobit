# Micro:bit czy mnie s�yszysz?

## Czego nauczysz si� w tym rozdziale?

* Jak u�ywa� modu�u radio
* Jak u�ywa� 2 lub wi�cej Micro:bit�w, �eby stworzy� sie� radiow�

## Czym jest modu� radio?

Wewn�trz ka�dego BBC Micro:bita znajduje si� bardzo interesuj�ca funkcjonalno��, kt�rej mo�emy u�y�, czyli - radio.

Mo�emy u�ywa� modu�u radio do wysy�ania i otrzymywania wiadomo�ci.

Co dalej?

Dobierzcie si� w kilkuosobowe grupy, i wybierzcie jaki� numer, kt�ry b�dzie u�ywany tylko w waszej grupie.

Je�li cz�onkowie grupy nie siedz� blisko to nic nie szkodzi, poniewa� mamy radio!

U�ywanie modu�u radio jest bardzo proste. Musimy:

1. Zaimportowa� modu� radio
2. W��czy� radio
3. Ustawi� numer grupy
4. Wysy�a� albo otrzymywa� wiadomo�ci

```python
import radio
import random
from microbit import display, Image, button_a, sleep

# Create the "flash" animation frames. Can you work out how it's done?
flash = [Image().invert()*(i/9) for i in range(9, -1, -1)]

# The radio won't work unless it's switched on.
radio.on()

# The radio won't work unless it's switched on.
radio.config(group=NumberThatYouChose)
# A micro:bit Firefly.

# Event loop.
while True:
    # Button A sends a "flash" message.
    if button_a.was_pressed():
        radio.send('flash')  # a-ha
    # Read any incoming messages.
    incoming = radio.receive()
    if incoming == 'flash':
        # If there's an incoming "flash" message display
        # the firefly flash animation after a random short
        # pause.
        sleep(random.randint(50, 350))
        display.show(flash, delay=100, wait=False)
        # Randomly re-broadcast the flash message after a
        # slight delay.
        if random.randint(0, 9) == 0:
            sleep(500)
            radio.send('flash')  # a-ha
```
