# Game and Watch Doom PSX Fire

Based on [Fabien Sanglad's blog post](https://fabiensanglard.net/doom_fire_psx/index.html) with a few tweaks. 

## Building
Clone Ghidra Ninja's [game-and-watch-base](https://github.com/ghidraninja/game-and-watch-base) and copy over main.c under the path `/Core/Src/`.
If not done, best to backup the firmware [here](https://github.com/ghidraninja/game-and-watch-backup) first.

## Release
Compiled image for the Game and Watch [here](https://github.com/x1sec/game-and-watch-doom-fire/releases/download/0.1/doom-fire.zip).
## Palette

Game and Watch LCD is only 12bit RGB, experiment with 12bit palette:
```
$ gcc gen_palette.c -o gen_palette
$ ./gen_palette
const uint16_t palette[] = {0,0,0,0,256,256,256,512,5 ....
```
replace `palette` in the relevant line in `main.c`
