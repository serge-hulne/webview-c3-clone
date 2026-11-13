# webview-c3 (forked)

- This is a fork of https://github.com/thechampagne/webview-c3 updated for C3 v. 0.8.6 (Linux and Mac OS)

- C3 binding for a tiny cross-platform **webview** library to build modern cross-platform GUIs.


### References
 - [webview]I (https://github.com/webview/webview)
 - [webview-c3] (https://github.com/thechampagne/webview-c3) 

### License

This repo is released under the [MIT License]


- ### Prerequisites

Build the static webview library:

```sh
git clone https://github.com/webview/webview
cd webview
cmake -G Ninja -B build -S . -D CMAKE_BUILD_TYPE=Release
cmake --build build
```

Copy `libwebview.a` (find it with `find build -name 'libwebview.a'`) to `/usr/local/lib`,
or set your own path with `"linker-search-paths"` in your `project.json`,
or put it in `webview.c3l/macos-aarch64/`.

Note: if `libwebview.dylib` sits in the same directory, the linker picks it
instead of the `.a`, and the program fails at launch with `Library not loaded: @rpath/...`.

### Build and run the example

```sh
cd examples/basic
c3c build
./build/basic
```
