import board

from kmk.kmk_keyboard import KMKKeyboard
from kmk.scanners.keypad import KeysScanner
from kmk.keys import KC
from kmk.modules.macros import Press, Release, Tap, Macros

keyboard = KMKKeyboard()

macros = Macros()
keyboard.modules.append(macros)

PINS = [board.D4, board.D5, board.D6, board.D7, board.D8, board.D9, board.D10]

keyboard.matrix = KeysScanner(
    pins=PINS,
    value_when_pressed=False,
)

# Look here for keycodes: https://github.com/KMKfw/kmk_firmware/blob/main/docs/en/keycodes.md
# And here for macros: https://github.com/KMKfw/kmk_firmware/blob/main/docs/en/macros.md
keyboard.keymap = [
    [KC.ENTER, KC.DELETE, KC.ESCAPE, KC.BSPACE, KC.TAB, KC.LSHIFT, KC.LCTRL, KC.LALT, KC.LGUI, KC.CAPSLOCK, KC.HOME, KC.END]
]

if __name__ == '__main__':
    keyboard.go()
