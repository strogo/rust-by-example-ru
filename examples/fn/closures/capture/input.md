Замыкания довольно гибкие и делают всё, что требуется для работы с ними без
дополнительных указаний. Это позволяет захватывать переменные, перемещая их или
заимствуя, в зависимости от необходимости.
Замыкания могут захватывать переменные:

* по ссылке: `&T`
* по изменяемой ссылке: `&mut T`
* по значению: `T`

Они преимущественно захватывают переменные по ссылке, если явно не указан другой
способ.

{capture.play}

### Смотрите также:

[`Box`][box] и [`std::mem::drop`][drop]

[box]: ../../std/box.html
[drop]: https://doc.rust-lang.org/std/mem/fn.drop.html
