# zig-pduarte

Learning Zig

[Zig Book by Pedro Duarte Faria](https://pedropark99.github.io/zig-book/)

I have already donated $10 for the book :)

## Ch. 1

### New project

```bash
mkdir hello_world
cd hello_world
zig init
```

- `main.zig` - main entry point of the program
- `root.zig` - root source file of the library

### Import

```zig
const std = @import("std");
```

### Errors

`!void` - returns either nothing or error

- add exclamation mark to return type so that it can return an error
- explicitly handle this error inside the function

```zig
const std = @import("std");

pub fn main() !void {
    const stdout = std.io.getStdOut().writer();
    try stdout.print("Hello, {s}!\n", .{"world"});
}
```

### Compilation

```bash
zig build-exe src/main.zig
```

- `build-exe`
- `build-lib`
- `build-obj`
- `run`
