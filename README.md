# collafl-dyninst
for no-pie binaries.

## Install Dyninst

[the branch](https://github.com/mxz297/dyninst/tree/rerewriting)

```
git clone https://github.com/mxz297/dyninst.git
cd dyninst
git checkout fuzzing
```
install:
[install instructions](https://github.com/mxz297/dyninst)

## environment
```
export DYNINST_INSTALL=/path/to/dynBuildDir
export COLL_PATH=/path/to/collafl-dyninst

export DYNINSTAPI_RT_LIB=$DYNINST_INSTALL/lib/libdyninstAPI_RT.so
export LD_LIBRARY_PATH=$DYNINST_INSTALL/lib:$COLL_PATH
export PATH=$PATH:$COLL_PATH
```


use dyninst to implement CollAFL

    ./CollAFLDyninst -i /path/to/target -o /path/to/instrumented/binary
