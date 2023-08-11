This project requires a custom RUSTFLAGS to compile.

`RUSTFLAGS="-L/opt/homebrew/opt/libomp/lib" cargo build --release`
works correctly, but
`RUSTFLAGS="-L/opt/homebrew/opt/libomp/lib" cargo test --doc`
will not build, with the error:
```
error: linking with `cc` failed: exit status: 1
          ...
          ld: library not found for -lomp
          clang: error: linker command failed with exit code 1 (use -v to see invocation)
```

Tested with Rust 1.71
