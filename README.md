# Audio
Not detecting audio device
```
pulseaudio -k && sudo alsa force-reload
```

# Input languages
* Settings > Regions and Languages > Manage installed languages > Install Vietnamese > Reboot
* Settings > Keyboard > Input Sources > Vietnamese (Unikey)
* Settings > Keyboard > Input Sources > Japanese (Mozc)

# Firefox
*about:config*
* browser.quitShortcut.disabled
* toolkit.tabbox.switchByScrolling

# Osu
### Opentabletdriver: tablet not detected
https://github.com/OpenTabletDriver/OpenTabletDriver/wiki/Linux-FAQ#argumentoutofrangeexception-value-0-15
```
echo "blacklist hid_uclogic" | sudo tee -a /etc/modprobe.d/blacklist.conf
sudo rmmod hid_uclogic
```
Replug tablet and reboot system if necessary.

### Keyboard only detect one button
press f10

### Sound problem
https://forums.lutris.net/t/bug-osu-game-sound-is-playing-like-the-devils-voice/11965

Lutris > osu > System Options > Scroll down to Enviroment tables > Click Add > set “key” to “PULSE_LATENCY_MSEC” > set its value to 6 > save
