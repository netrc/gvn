
## gvn

simplistic tool to
* generate/bump version numbers
* put tag in git
* keep module up-to-date with importable strings to display


### basic plan
* 'gvn' bumps version number string in gvn.js  (or .py...)
* commit your source (which commits version number string in gvn.js)
* tags previous commit with the version number string

You can then...
* display version number (and date) in your program/gui
* find the version number tag in git
