# Define & Run Async Host Functions

This example demonstrates how to define async host functions, and register and run it over WasmEdge Runtime.

Now let's build and run this example.

- Install `rustup` and `Rust`

  Go to the [official Rust webpage](https://www.rust-lang.org/tools/install) and follow the instructions to install `rustup` and `Rust`.

  > It is recommended to use Rust 1.71 or above in the stable channel.

  Then, add `wasm32-wasi` target to the Rustup toolchain:

  ```bash
  rustup target add wasm32-wasi
  ```

- Install WasmEdge Runtime

  Refer to the [Quick Install](https://wasmedge.org/book/en/quick_start/install.html#quick-install) section of WasmEdge Runtime Book to install WasmEdge Runtime. Or, use the following command directly

  ```bash
  # NOTICE that the installation script needs `sudo` access

  # install wasmedge to the directory /usr/local/
  curl -sSf https://raw.githubusercontent.com/WasmEdge/WasmEdge/master/utils/install.sh | bash -s -- -v 0.14.0
  source $HOME/.wasmedge/env
  ```

  > For users in China mainland (中国大陆地区), try the following command to install WasmEdge Runtime if failed to run the command above
  >
  > ```bash
  > # NOTICE that the installation script needs `sudo` access
  >
  > bash install_zh.sh -v 0.14.0
  > source $HOME/.wasmedge/env
  > ```

- Download example

  ```bash
  git clone git@github.com:second-state/wasmedge-rustsdk-examples.git
  cd wasmedge-rustsdk-examples/define-async-host-func
  ```

- Build & run

  ```bash
  cargo run
  ```

  If the command runs successfully, then the following result is printed out on the screen:

  ```bash
  [tick] i=0
  [async hello] say hello
  [tick] i=1
  [async hello] say hello
  [tick] i=2
  [tick] i=3
  [async hello] say hello
  [tick] i=4
  [tick] i=5
  [async hello] say hello
  [tick] i=6
  [tick] i=7
  [async hello] say hello
  [tick] i=8
  [tick] i=9
  [async hello] say hello
  [tick] i=10
  [tick] i=11
  [async hello] say hello
  [tick] i=12
  [tick] i=13
  [async hello] say hello
  [tick] i=14
  [tick] i=15
  [async hello] say hello
  [tick] i=16
  [tick] i=17
  [async hello] say hello
  [tick] i=18
  [tick] i=19
  [async hello] Done!
  ```
