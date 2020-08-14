# LaTeX Concealer for Sublime-Text-3
LaTeX concealer for sublime-text-3

![LaTeX concealer demo](https://github.com/rah4927/demo/blob/master/conceal_tex.gif)

This is a personal project to replicate some of vim's <b>conceal</b> features in sublime text 3. The current version uses a combination of syntax fold, manipulating the color of the fold icon, and phantom objects in sublime to conceal code. Working on making it real-time, and adding more LaTeX substitutions.

## How To Use 

1. Download and put the files in ```~/.config/sublime-text-3/Packages/User```. 
2. Edit the user defined keybindings file and add  ``` { "keys": ["ctrl+shift+d"], "command": "texconceal" } ```
3. Now edit your TeX file, and use the keybinding in the line you want to conceal. 

## Tips 

In order to make folding distraction free, try looking up the background color in your color scheme and change the fold icon to have the same color. This makes it coalesce with the background.

## Editing 

If you want to edit the files as your own, here is a brief explanation of the files: 

1. ```latexparser.py``` is a DFA that takes in a latex command and separates it into <b>commands</b> and <b>arguments</b> 
2. ```latex2utf.py``` takes in a latex command and translates it into UTF-8 
3. ```TeXconceal.py``` is the plugin that defines the text command ```texconceal``` 
4. ```behindFold.py``` is an additional plugin that prevents folded text from being deleted 
5. ```LaTeX substitutions.json``` contains a dictionary of commands and substitutions 

## Shortcomings 

1. No real-time sync 
2. I haven't hardcoded behviour of ```\text{}, \frac{}{}, \dfrac{}{}``` yet  
