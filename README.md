# ArchLinux
## Perron
### Seguimos la guia del primo s4vitar https://www.youtube.com/watch?v=fshLf6u8B-w

Como los repos estan actualizados del payo del awesome a mi me dio problemas https://github.com/rxyhn/dotfiles 
> No me dejaba seleccionar awesome en el login

Asi que seguí el man del repo del dotfile y además como me daba error el noseque del audio lo solucioné así tomando como referencia la snap intale todo lo de la guia y ademas esto.
```bash
$ git clone https://aur.archlinux.org/snapd.git
cd snapd
makepkg -si

$ sudo systemctl enable --now snapd.socket

$ sudo ln -s /var/lib/snapd/snap /snap
```
