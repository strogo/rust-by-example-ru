В некоторых случаях использование `match` выглядит неуклюже. Например:

```rust
// Создадим переменную `optional` с типом `Option<i32>`
let optional = Some(7);

match optional {
    Some(i) => {
        println!("Это действительно очень длинная строка и `{:?}`", i);
        // ^ Необходимо два вложения для того, чтобы просто деструктурировать
        // `i` из опционального типа.
    },
    _ => {},
    // ^ Требуется, потому что `match` должен учесть все варианты. Вам не кажется
    // это немного лишним?
};

```

`if let` намного компактнее и выразительнее для данного случая и, кроме того, 
позволяет рассмотреть различные варианты ошибок.

{if_let.play}

### Смотрите также:

[`enum`][enum], [`Option`][option], and the [RFC][if_let_rfc]

[enum]: ../custom_types/enum.html
[if_let_rfc]: https://github.com/rust-lang/rfcs/pull/160
[option]: ../std/option.html
