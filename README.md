# Requirements

* cmake (as build system)
* OpenSSL
* Pthreads (for POSIX systems it's builtin, for Windows there's a library)

```
git submodule init
git submodule update
mkdir _build && cd _build
cmake ../
cmake --build ./
```
## Example on Windows
```
cmake ../ -G "Visual Studio 15 2017 Win64" -DPTHREAD_INCLUDE_DIR=C:\pthread-x64\include -DPTHREAD_LIBRARY=C:\pthread-x64\lib\pthread_lib.lib
```


# BOOST



b2 --toolset=msvc-14.2 link=static runtime-link=static address-model=64 define=BOOST_USE_WINAPI_VERSION=0x0501 --with-chrono --with-date_time --with-filesystem --with-program_options --with-system