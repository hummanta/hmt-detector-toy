# hmt-detector-toy

A simple CLI tool to detect Toy files by checking if a given path contains
any `.toy` files.

## Installation

Prebuilt binaries Windows, Linux and macOS can be downloaded from the [Github
release
page](https://github.com/hummanta/hmt-detector-toy/releases/latest). If
there is no distro package available in your preferred manager, you need [Rust
and cargo](https://www.rust-lang.org/tools/install) to build it.

### Install from source:

1. Clone the repository with `git clone
   https://github.com/hummanta/hmt-detector-toy.git`
2. From the `hmt-detector-toy` directory, run `cargo build --release` to
   build the application in release mode.
3. After a successful compilation, launch the executable with:
   `target/release/hmt-detector-toy`.

### Install with cargo

To get the latest bug fixes and features, you can install the development
version from git. However, this is not fully tested. That means you're probably
going to have more bugs despite having the latest bug fixes.

```
cargo install --git https://github.com/hummanta/hmt-detector-toy
```

This will download the source from the main branch, build and install it in
Cargo's global binary directory (`~/.cargo/bin/` by default).

## Usage

```text
Usage: hmt-detector-toy [OPTIONS]

Options:
      --path <PATH>  The path to the file or directory to detect [env: DETECT_PATH=]
  -h, --help         Print help
```

Example:

```bash
hmt-detector-toy --path path/to/toy-file.toy
```

This will output a JSON result:

```json
{
  "pass": true,
  "language": "Toy"
}
```

## Development

To build this project, you will need to install the following pre-requisites:
[Git](https://git-scm.com/downloads),
[Rust](https://www.rust-lang.org/tools/install) and
[Just](https://github.com/casey/just).

After cloning the repository, you can simply run `just` in the package directory
to list all available commands. For your first local build, please run `just
install` command to install the dependencies for this project.

## Contributing

If anything feels off, or if you feel that some functionality is missing, please
check out the [contributing page](CONTRIBUTING.md). There you will find
instructions for sharing your feedback, building the project locally, and
submitting pull requests to the project.

## License

Copyright (c) The Hummanta Authors. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
