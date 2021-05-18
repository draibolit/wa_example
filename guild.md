## Ref
https://www.syntaxsuccess.com/viewarticle/combining-c-plus-plus-with-javascript
https://ihsavru.medium.com/loading-webassembly-modules-in-javascript-dc09fbd5eac2

## Install emscripten

Get the emsdk repo
git clone https://github.com/emscripten-core/emsdk.git

Enter that directory
cd emsdk
 Fetch the latest version of the emsdk (not needed the first time you clone)
git pull

 Download and install the latest SDK tools.
./emsdk install latest

 Make the "latest" SDK "active" for the current user. (writes .emscripten file)
./emsdk activate latest

 Activate PATH and other environment variables in the current terminal
source ./emsdk_env.sh
https://emscripten.org/docs/getting_started/downloads.html

## Build
```
cd ./build
emcmake cmake ..
make
```

