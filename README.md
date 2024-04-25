
# mel's wmx dots!

As the name implies, these dotfiles are for my wmx setup.
wmx is an absolutely awesome X window manager that has some really cool features, most notably these beautiful titlebars & window borders:

![screenshot](https://cdn.discordapp.com/attachments/822517913914834984/1232700421810684018/Screenshot_2024-04-25-02-30-47_1920x1200.png?ex=662a693b&is=662917bb&hm=de9b78434dcf087b823606365b34046d8a0c8178886926d82bd5964bf6472f43&)



## Components

My dotfiles are made up of a good number of things for one main reason, and that is to act as a substitute for all the features that wmx **doesn't** have.

You'll need all of these things on your system for these dots to work properly.

**[dunst](https://github.com/dunst-project/dunst)** for notifications

**[rofi](https://github.com/davatorium/rofi)** for an application launcher and screenshot menu

**[sxhkd](https://github.com/baskerville/sxhkd)** to manage hotkeys

**[xst](https://github.com/gnotclub/xst)** as a terminal emulator with support for xresources

**[wmx](https://www.all-day-breakfast.com/wmx/)** as the window manager

**[wmclock](https://www.dockapps.net/wmclock)** as a floating desktop clock

**[cozette](https://github.com/slavfox/Cozette)** as the main font
    
**Prima Serif Bold** as the titlebar font 

I use `base16-greyscale-dark` as the colorscheme for this whole setup. 

You can find a *multitude* of configurations with this colorscheme under the [base16](https://github.com/topics/base16) topic on GitHub.
## Installation

Firstly, you will have to build wmx from source, as there are no prepackaged binaries.

I have provided my `Config.h` file in the `wmx-files` directory in this repository, which is what's used to configure fonts, keybinds and other preferences. You can change this, if you'd prefer. 

I'd **highly** recommend you change the keybinds in both `Config.h` and `sxhkd/sxhkdrc`, as I use some pretty strange ones.

```bash
  git clone https://github.com/m3lpomene/wmx-rice.git
  cd wmx-rice
  wget https://www.all-day-breakfast.com/wmx/wmx-8.tar.gz
  tar -xzvf wmx-8.tar.gz
  cd wmx-8
  mv ../wmx-rice/wmx-files/Config.h Config.h
  ./configure
  make
```

You have built wmx, and now have an executable and a `wmx.desktop` file in the directory. Disregard the latter. wmx does not have any autostart functions, so we'll be using our own. 

We'll be manually moving both the wmx executable and the `wmx.desktop` file to their respective locations.

I've provided my own `wmx.desktop` file in the `wmx-8` directory, which you should probably use.

```bash
   sudo mv wmx /usr/local/bin/wmx
   sudo mv ../wmx-rice/wmx-8/wmx.desktop /usr/share/xsessions 
```

While you're here, install Prima Serif Bold, which is unavailable elsewhere
```bash
   mv ../wmx-rice/fonts/PrimaSerifBold.otf ~/.local/share/fonts
   fc-cache -f -v
```

Now that you have wmx installed on your system, you can start creating the directory it's files are going to sit in.

```bash
 cd ..
 mkdir ~/.wmx
 mv * ~/.wmx
```


Assuming you have all the other dependencies installed.. you are pretty much done! 

At this point you should probably login, play around a bit, read the README in the wmx directory you built from, and change whatever you find unappealing. 
## Credits

 - [adi1090x](https://github.com/adi1090x) who I shamelessly stole the rofi screenshot script & dunstrc from, more specifically from his [Blackbox](https://github.com/archcraft-os/archcraft-blackbox) directory.
 
- [inkai](https://instagram.com/_inkai) for her beautiful art used in the first screenshot

## Screenshots

![desktop](https://cdn.discordapp.com/attachments/1039735868564439083/1230083214354288701/xRTQkjF.png?ex=662a1e44&is=6628ccc4&hm=1ff0fb67438a62f4bf6887b263934e934fb67e20756c9fb54dc8b2018d3a285a&)



![desktop-rofi](https://cdn.discordapp.com/attachments/1229692076015357962/1229692605705748561/lbELaRy.png?ex=662a03fb&is=6628b27b&hm=832a1fb9edead511c32b5dc208c1ac141732c83706268d55c9ab87b436951708&)