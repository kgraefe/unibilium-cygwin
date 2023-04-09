# unibilium-cygwin

This a recipe to build and package [Unibilium][1] for [Cygwin][2]. The recipe
is based on the [recipe in cascent's old neovim port][3].

To build the package run the following command:
```sh
cygport unibilium.cygport download prepare compile install package
```

To install the package you can extract it into the root directory:
```sh
eval "$(cygport unibilium.cygport vars PVR)"
tar -C / -xjvf unibilium-$PVR.x86_64/dist/unibilium/libunibilium4/libunibilium4-$PVR.tar.xz
```

[1]: https://github.com/mauke/unibilium
[2]: http://www.cygwin.com/
[3]: https://github.com/cascent/neovim-cygwin/blob/09277e3f76981189a2f15d1dbc2f5a4ab4b6c86f/unibilium/unibilium.cygport
