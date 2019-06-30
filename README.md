# go-wasm-obj-analyser

A simple tool to get a per-package size distribution of a Go WASM binary.

## Installation

```
go get -u github.com/Ackar/go-wasm-obj-analyzer
```

`go-wasm-obj-anaylser` reads the output of `wasm-objdump` which is available
as part of the [WebAssembly Binary Toolkit (WABT)](https://github.com/WebAssembly/wabt).

## Example usage

```
$> wasm-objdump -d main.wasm | go-wasm-obj-analyser                                                                       scleymans@scleymans
Total size: 1.2 MB
Package runtime is 693 kB
Package reflect is 168 kB
Package fmt is 85 kB
Package unicode is 53 kB
Package type is 52 kB
Package strconv is 46 kB
Package syscall_js is 33 kB
Package sync is 23 kB
Package internal_fmtsort is 18 kB
Package syscall is 11 kB
Package os is 8.5 kB
Package internal_poll is 8.0 kB
Package unicode_utf8 is 5.8 kB
Package sort is 4.8 kB
Package internal_cpu is 4.3 kB
Package runtime_internal_atomic is 3.2 kB
Package time is 3.0 kB
Package sync_atomic is 2.1 kB
Package runtime_debug is 2.0 kB
Package io is 1.8 kB
Package main is 514 B
Package errors is 451 B
Package memchr is 267 B
Package callRet is 114 B
Package memcmp is 74 B
Package memeqbody is 68 B
Package internal_bytealg is 67 B
Package cmpbody is 56 B
Package wasm_export_run is 45 B
Package _rt0_wasm_js is 21 B
Package wasm_export_resume is 19 B
Package wasm_pc_f_loop is 19 B
Package wasm_export_getsp is 3 B
Package go is 2 B
```
