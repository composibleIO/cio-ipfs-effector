Cloned from https://github.com/fluencelabs/ipfs-effector with minor tweaks: 

* changed CONNECT_TIMEOUT to 30s. 
* extended build.sh to copy wasm file into a folder with a module.yaml file .. so it can be included in a project

```
cd cio-ipfs-effector
. build.sh
```

cid = bafkreic43ajmlqhna7xrdadnbkfcsecygl43jmjqajz5xyyhoypfo563qe

how i use it in a project: 

```
ln -s ../../cio-ipfs-effector/module <myService>/modules/cio-ipfs-effector
```