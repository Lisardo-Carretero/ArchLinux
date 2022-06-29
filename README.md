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
## Las fonts
> seguimos con el tuto del savitar

descargar wget e instalar en ` /usr/share/fonts` como ` sudo `
```bash
$ wget https://fontlot.com/downfile/5baeb08d06494fc84dbe36210f6f0ad5.105610
```
Despues pasamos los archivos que queremos al derectorio de fonts y borramos lo que no necesitamos
```bash
$ find . | grep "\.ttf$" | while read line; do cp  $line .; done
$ rm -r iosevka-2.2.1/
$ rm -r iosevka-slab-2.2.1/
```
Nos bajamos el archivos de dropbox `https:://dropbox.com/s/hrkub2yo9iapljz/icomoon.zip?dl=0`
> icomoon

Descomprimes y mueves todo lo que acabe en ttf a este directorio 

Ahora instalamos mas fuente
```bash
$ paru -S nerd-fonts-jetbrains-mono ttf-font-awesome ttf-font-awesome-4 ttf-material-design-icons
```
Te mueves al directorio de los repos `/home/Desktop/$user/repos/` y lanzamos los comandos
```bash
$ git clone --recurse-submodules https://github.com/rxyhn/dotfiles.git
$ cd dotfiles && git submodule update --remote --merge
```
y copiamos la configuracion correspondiente
```bash
$ cp -r config/* ~/.config/
```
