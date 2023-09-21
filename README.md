# rust + wasm

## tutorial

1. Before you start, make sure you have the `wasm-wasi` target installed:
```bash
rustup target add wasm32-wasi
```

2. Within the source directory of a cargo project, use cargo or rustc to compile to wasm:

```bash
cargo build --target wasm32-wasi
```

3. Install the `wasmtime` runtime on linux/mac/wsl2:

```bash
curl https://wasmtime.dev/install.sh -sSf | bash
```

4. Run the `.wasm` target using the `wasmtime` cli runner:

```bash
wasmtime target/wasm32-wasi/debug/rust-wasm-runtime.wasm
```

### using rustc

1. build

```bash
rustc main.rs --target wasm32-wasi
```

2. run

```bash
wasmtime main.wasm
```

## resources
- Command line runner: [wasmtime](https://wasmtime.dev/)
- Rust Compilation targets: [docs](https://doc.rust-lang.org/nightly/rustc/platform-support.html)