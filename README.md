from https://medium.com/@arora.aashish/webassembly-dynamic-linking-1644c9f40c8c

# bonus to debug with source code
```
mkdir assets
emcc cuberoot.cc -s EXPORT_ALL=1 -s SIDE_MODULE=1 -o assets/cuberoot.wasm -gsource-map --source-map-base /
emcc main.cc -s MAIN_MODULE=1 --preload-file ./assets/cuberoot.wasm --bind -gsource-map --source-map-base /
```