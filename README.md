# jupyterthemes
## Theme-ify your Jupyter Notebooks!

|Author | Version | Status | Demo |
|:--------------------:|:------------:|:------------:|:------------:|
|  Kyle Dunovan | ![image](https://img.shields.io/pypi/v/jupyterthemes.svg) | ![image](https://travis-ci.org/dunovank/jupyter-themes.svg?branch=develop) | [![Binder](http://mybinder.org/badge.svg)](http://mybinder.org:/repo/dunovank/jupyter-themes) |

###### *figures (coming soon)*
![image](screens/onedork_figure_style.png)

###### *markdown/equations*
![image](screens/oceans16_markdown.png)

###### *pandas dataframes*
![image](screens/grade3_table.png)

###### *command palette*
![image](screens/oceans16_command_palette.png)

###### *oceans16 syntax*
![image](screens/oceans16_code_headers.png)

###### *grade3 syntax*
![image](screens/grade3_code_headers.png)

###### *onedork syntax*
![image](screens/onedork_code_headers.png)

###### *chesterish syntax*
![image](screens/chesterish_code_headers.png)

### Links
* [jupyterthemes on PyPI](https://pypi.python.org/pypi/jupyterthemes/)
* [jupyterthemes on GitHub](https://github.com/dunovank/jupyter-themes)

### Requirements
* Python 2.7, 3.3, 3.4, or 3.5
* Jupyter ([Anaconda](https://www.continuum.io/downloads) recommended)

### Install with pip
```sh
# install/upgrade to latest version
pip install --upgrade jupyterthemes
```

### Known issues
* Depending on your system, browser, etc., you may need to empty your browser cache after installing a new theme (-t) or attempting to restore the default (-r) in order for those changes to take effect. (see discussion [here](https://github.com/dunovank/jupyter-themes/issues/86))
* If emptying the cache doesn't work, you may need to start a new jupyter session or restart your browser (see discussion [here](https://github.com/dunovank/jupyter-themes/issues/92))
* Some users have found that "jt" is not recognized after installing the pypi release (as shown above). Still trying to get to the bottom of this but apparently the following provides a temporary fix (see discussion [here](https://github.com/dunovank/jupyter-themes/issues/92#issuecomment-277461319)).

```sh
# uninstall any existing versions
pip uninstall jupyterthemes
# install from the github repo
pip install --user git+https://github.com/dunovank/jupyter-themes.git

```


### Command Line Usage
```
usage: jt [-h] [-l] [-t THEME] [-f MONOFONT] [-fs MONOSIZE] [-nf NBFONT]
          [-nfs NBFONTSIZE] [-tf TCFONT] [-tfs TCFONTSIZE] [-m MARGINS]
          [-cursw CURSORWIDTH] [-cursc CURSORCOLOR] [-cellw CELLWIDTH]
          [-lineh LINEHEIGHT] [-alt] [-vim] [-T] [-N] [-r]
```
|        options        |   arg     |     default   |
|:----------------------|:---------:|:-------------:|
| Usage help            |  -h       |      --       |
| List Themes           |  -l       |      --       |
| Theme Name to Install |  -t       |      --       |
| Code Font             |  -f       |    source     |
| Code Font-Size        |  -fs      |      11       |
| Notebook Font         |  -nf      |    exosans    |
| Notebook Font Size    |  -nfs     |      13       |
| Text/MD Cell Font     |  -tf      |  merriserif   |
| Text/MD Cell Fontsize |  -tfs     |      13       |
| Intro Page Margins    |  -m       |     auto      |
| Cell Width            |  -cellw   |      980      |
| Line Height           |  -lineh   |      170      |
| Cursor Width          |  -cursw   |       2       |
| Cursor Color          |  -cursc   |      --       |
| Alt Text/MD Layout    |  -alt     |      --       |
| Alt Prompt Layout     |  -altp    |      --       |
| Style Vim NBExt*      |  -vim     |      --       |
| Toolbar Visible       |  -T       |      --       |
| Name & Logo Visible   |  -N       |      --       |
| Restore Default       |  -r       |      --       |

### Examples
```sh
# list available themes
# oceans16 | grade3 | chesterish | onedork | monokai | solarized-light
jt -l

# select theme...
jt -t chesterish

# restore default theme
# NOTE: Need to delete browser cache after running jt -r
# If this doesn't work, try starting a new notebook session.
jt -r

# toggle toolbar ON and notebook name ON
jt -t grade3 -T -N

# set code font to 'Roboto Mono' 12pt
# (see monospace font table below)
jt -t oceans16 -f roboto -fs 12

# set code font to Fira Mono, 11.5pt
# 3digit font-size gets converted into float (115-->11.5)
jt -t grade3 -f fira -fs 115

# set text-cell/markdown and notebook fonts
# (see sans-serif & serif font tables below)
jt -t onedork -tf georgiaserif -nf droidsans

# adjust cell width, line-height of codecells
jt -t chesterish -cellw 900 -lineh 170

# fix the container-margins on the intro page (defaults to 'auto')
jt -t onedork -m 200

# adjust cursor width (in px) and make cursor red (r)
# options: b (blue), o (orange), r (red), p (purple), g (green)
jt -t grade3 -cursc r -cursw 5

# toggle toolbar ON and notebook name ON
jt -t grade3 -T -N

# choose alternate txt/markdown layout (-alt)
# and alternate cell prompt (narrow, no numbers)
jt -t grade3 -alt -altp
```

### Monospace Fonts (code cells)
| -f arg | Monospace Font |
|:--|:--|
|anka|Anka/Coder|
|anonymous|Anonymous Pro|
|aurulent|Aurulent Sans Mono|
|bitstream|Bitstream Vera Sans Mono|
|bpmono|BPmono|
|code|Code New Roman|
|consolamono|Consolamono|
|cousine|Cousine|
|dejavu|DejaVu Sans Mono|
|droidmono|Droid Sans Mono|
|fira|Fira Mono|
|firacode|Fira Code|
|generic|Generic Mono|
|hack|Hack|
|inconsolata|Inconsolata-g|
|inputmono|Input Mono|
|liberation|Liberation Mono|
|meslo|Meslo|
|office|Office Code Pro|
|oxygen|Oxygen Mono|
|roboto|Roboto Mono|
|saxmono|saxMono|
|source|Source Code Pro|
|sourcemed|Source Code Pro Medium|
|ptmono|PT Mono|
|ubuntu|Ubuntu Mono|

### Sans-Serif Fonts
| -nf/-tf arg | Sans-Serif Font |
|:--|:--|
|exosans|Exo_2|
|opensans|Open Sans|
|droidsans|Droid Sans|
|latosans|Lato|
|ptsans|PT Sans|
|robotosans|Roboto|
|sourcesans|Source Sans Pro|
|amikosans|Amiko|
|nobilesans|Nobile|
|alegreyasans|Alegreya|
|armatasans|Armata|
|cambaysans|Cambay|
|catamaransans|Catamaran|
|franklinsans|Libre Franklin|
|frankruhlsans|Frank Ruhl|
|gothicsans|Carrois Gothic|
|gudeasans|Gudea|
|hindsans|Hind|
|jaldisans|Jaldi|
|makosans|Mako|
|merrisans|Merriweather Sans|
|mondasans|Monda|
|oxygensans|Oxygen Sans|
|pontanosans|Pontano Sans|
|puritansans|Puritan Sans|
|ralewaysans|Raleway|

### Serif Fonts
| -nf/-tf arg | Serif Font |
|:--|:--|
|loraserif|Lora|
|andadaserif|Andada|
|arapeyserif|Arapey|
|ptserif|PT Serif|
|georgiaserif|Georgia|
|cardoserif|Cardo|
|crimsonserif|Crimson Text|
|droidserif|Droid Serif|
|ebserif|EB Garamond|
|merriserif|Merriweather|
|notoserif|Noto Serif|
|vesperserif|Vesper Libre|
|scopeserif|ScopeOne|
|sanchezserif|Sanchez|
|neutonserif|Neuton|
|rasaserif|Rasa|
|goudyserif|Sorts Mill Goudy|
|vollkornserif|Vollkorn|
