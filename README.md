# async-executor

[![Build](https://github.com/smol-rs/async-executor/workflows/Build%20and%20test/badge.svg)](
https://github.com/smol-rs/async-executor/actions)
[![License](https://img.shields.io/badge/license-MIT%2FApache--2.0-blue.svg)](
https://github.com/smol-rs/async-executor)
[![Cargo](https://img.shields.io/crates/v/async-executor.svg)](
https://crates.io/crates/async-executor)
[![Documentation](https://docs.rs/async-executor/badge.svg)](
https://docs.rs/async-executor)

Async executors.

## Examples

```rust
use async_executor::Executor;
use futures_lite::future;

// Create a new executor.
let ex = Executor::new();

// Spawn a task.
let task = ex.spawn(async {
    println!("Hello world");
});

// Run the executor until the task completes.
future::block_on(ex.run(task));
```

## License

Licensed under either of

 * Apache License, Version 2.0 ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

#### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license, shall be
dual licensed as above, without any additional terms or conditions.
