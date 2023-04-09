# cutmidel in C++

An experiment to rewrite [cutmidel] from C to C++.

The code is a little shorter and simpler to write and the size didn't grow much.

| Language |  Size [B] |  Speed [ms] |
|----------|----------:|------------:|
| C        |    49,928 |      0.0055 |
| C++      |    53,104 |      0.0055 |
| Rust     |   300,368 |      0.0060 |
| V        |   490,832 |      0.0075 |
| Zig      |   877,054 |      0.0060 |
| Go       | 1,983,776 |      0.0070 |

See the others in [Rust], [V], [Zig] and [Go].

## Build

    mkdir build
    cd build
    cmake ..
    make
    ./cutmidel longtest 1 2

[cutmidel]: https://github.com/prantlf/cutmidel
[Rust]: https://github.com/prantlf/rust-cutmidel
[V]: https://github.com/prantlf/v-cutmidel
[Go]: https://github.com/prantlf/go-cutmidel
[Zig]: https://github.com/prantlf/zig-cutmidel
