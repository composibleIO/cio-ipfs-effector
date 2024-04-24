Cloned from https://github.com/fluencelabs/ipfs-effector with minor tweaks: 

* changed CONNECT_TIMEOUT to 30s. 
* extended build.sh to copy wasm file into a folder with a module.yaml file .. so it can be included in a project

```
cd cio-ipfs-effector
. build.sh
```

Custom effectors may only work in a local network. To whitelist the module add its CID to provider.yaml: 

```
nox:
  effectors:
    ipfs:
      wasmCID: <module-cid>
      allowedBinaries:
        ipfs: /usr/bin/ipfs

offers:
    effectors:
      - <module-cid>

```

how i use it in a project: 

```
ln -s ../../cio-ipfs-effector/module <myService>/modules/cio-ipfs-effector
```

