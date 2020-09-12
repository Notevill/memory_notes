# Про настройку переключения языков

За настройку переключения языков на X системах отвечает `setxkbmap`. Смотри на [arch wiki](https://wiki.archlinux.org/index.php/Xorg/Keyboard_configuration).

Параметры можно задать как, при запуске `setxkbmap` с параметрами, так и в конфигах X.

В файл `/etc/X11/xorg.conf.d/00-keyboard.conf` записываем:

```
Section "InputClass"
	Identifier "sustem-keyboard"
	MatchIsKeyboard "on"
	Option "XkbLayout" "us,ru"    # включаем языки us/ru
    Option "XkbModel" "pc105"   # модель клавиатуры, я даже не знаю, где нужно вставлять другую модель
    Option "XkbOptions" "grp:shift_caps_switch"   # перключения языка по CapsLock - us ; CapsLock+Shift - ru
EndSection
```
