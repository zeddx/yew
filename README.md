# Yew

Elm like framework, but for Rust and WASM revolution.

## Minimal application

```rust
extern crate yew;

use yew::html;

struct Model {
    value: u8,
}

enum Msg {
    Increment,
    Decrement,
}

fn update(model: &mut Model, msg: Msg) {
    match msg {
        Msg::Increment => {
            model.value = model.value + 1;
        }
        Msg::Decrement => {
            model.value = model.value - 1;
        }
    }
}

fn view(model: &Model) -> html::Html<Msg> {
    use html::*;
    unimplemented!();
}

fn main() {
    let model = Model {
        value: 0,
    };
    html::program(model, update, view);
}
```