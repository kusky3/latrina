# latrina
### WARNING: schizo repo, ignore
bypass url encoding for nontrivial shell commands

# cheatsheet  
### setting string variables without quotes    
`a="test"`            # nope  
`variable=('test')`   # yikes  
### separating fields without spaces  
`echo $a`             # nope   
`echo$IFS$a`          # yikes   
### piping without pipes  
`ls | wc -l`          # nope   
`wc -l < <(ls)`       # yikes  
### concatenating variables to strings
`echo $IFStest`       # nope
`a=('a');echo$IFS$a`  # yikes
