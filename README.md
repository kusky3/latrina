# latrina
bypass url encoding for nontrivial shell commands

# cheatsheet  
### setting string variables without quotes    
`a="test"`  
`variable=('test')`  
### separating fields without spaces  
`echo $a`  
`echo$IFS$a`
### piping without pipes  
`ls | wc -l`      
`wc -l < <(ls)`     
### concatenating variables to strings
`echo$IFSa`     
`a=('a');echo$IFS$a` 
