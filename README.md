# latrina
bypass url encoding with nontrivial commands

* click on the "Go to file" button
* click on the weirdly named file
* look at the address bar
* the url isn't sanitized

Brainlets like LTT will copy the url and eventually execute the payload,  
since they don't know about the "raw" button.  
Bypassing the rookie level will get you to this point.  
Bypassing the god-like level will get you the same,   
but on the raw content page, which is way nastier.  

# bypassed
```
'"' # needed to set string variables, bypassed with ('variable')
'{' # needed for ${IFS}, bypassed by concatenating $ or - after them
'}' # same as above
'|' # needed for command1 | command2, bypassed with command2 < <(command1)
' ' # needed as arguments separator, bypassed with $IFS
```

# todo
rookie level:
```
'<'
```

god-like level:
```
'$'
';'
'<'
'>'
```
