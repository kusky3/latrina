# latrina
bypass url encoding for nontrivial shell commands

# cheatsheet  
### setting string variables without quotes    
❌`a="a"`  
✅`variable=('a')`  
### separating fields without spaces 
❌`echo $a`  
✅`echo$IFS$a`
### separating fields without spaces and curly brackets
❌`echo${IFS}a`     
✅`a=('a');echo$IFS$a` 
### piping without pipes  
❌`ls | wc -l`      
✅`wc$IFS-l$IFS<$IFS<(ls)`     

