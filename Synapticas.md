#Тачпад Synaptics

Настройки тачпада мы заносим в конфигурацию Xorg

В файл `/etc/X11/xorg.cond.d/50-synaptics.conf` записать следующее:

```
Section "InputClass"
	Identifier "touchpad"
	Driver "synaptics"
	MatchIsTouchpad "on"
		Option "TapButton1" "1"		# тап 1 пальцем левый клик
		Option "TapButton2" "3"		# тап 2 пальзацами правый клик
		Option "TapButton3" "2"		# тап 3 пальзацми средний клик
		Option "VertTwoFingerScroll" "on"	# разрешить вертикальную прокрутку двумя пальщацми
		Option "HorizTwoFingerScroll" "on"	# разрешить горизонтальную прокрутку двумя пальцами
EndSection
```

Так же смотри [arch wiki](https://wiki.archlinux.org/index.php/Touchpad_Synaptics)
