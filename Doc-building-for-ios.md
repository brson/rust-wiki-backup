This currently does not work.

See some approaches: https://github.com/mozilla/rust/issues/6170

## Options

### Option 1: C-code from Rust's LLVM bitcode

1. Produce a `foo.ll` from a `foo.rs`:
  1. `rustc foo.rs -o foo.stage2 -O --save-temps`
  1. `llvm-dis foo.bc`
1. Create `foo.c` from `foo.ll`:
  1. TODO: something using `llc`

### Option 2: Rust's Android-ARM assembler code

### Option 3: Native iOS-support

## Resources

* [llc](http://llvm.org/docs/CommandGuide/llc.html)
* [llvm-dis](http://llvm.org/docs/CommandGuide/llvm-dis.html)
* [[Note seeing LLVM output from rust]]