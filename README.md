# Maximized Window Gap

>*This is a reduced version of **[Window Gaps](https://github.com/nclarius/tile-gaps)** script by **Natalie Clarius**.  
All credit goes to respective owner.*

Extension for KDE's window manager to add space around maximized windows.

![screenshot](.img/screenshot.png)

The size of the gaps are configurable.

![screenshot](.img/config.png)

## Installation

### Dependencies

`kwin` version ≥ 5.21.

### Method 1: via graphical interface

1. Install the script via *System Settings* > *Window Management* > *KWin Scripts* > *Get New Scripts …* > search for *Maximized Window Gap* > *Install*.
2. Activate the script by selecting the checkbox in the *Maximized Window Gap* entry.

### Method 2: via command line

```bash
git clone https://github.com/murat-cileli/maximized-window-gap.git
plasmapkg2 --type kwinscript -i maximized-window-gap
qdbus org.kde.KWin /KWin reconfigure
```

## Configuration

*System Settings* > *Window Management* > *KWin Scripts* > configuration button in the *Maximized Window Gap* entry.

You may have to disable the script, apply, reenable, and reapply in order for the changes to take effect.

If the configuration button is missing (this is due to a central limitation with the KWin script installation component), try the following:

````bash
mkdir -p ~/.local/share/kservices5
ln -sf ~/.local/share/kwin/scripts/maximized-window-gap/metadata.desktop ~/.local/share/kservices5/maximized-window-gap.desktop
````
