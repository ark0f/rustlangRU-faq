# faq

## Как установить Rust?

Официально рекомендуемый способ установки - [rustup.rs](https://rustup.rs).

## Какую версию использовать, stable, nightly?

Для новичков лучше всего подойдет последний stable.

## Что почитать по Rust?

Начинать лучше всего с [официальной книги](https://doc.rust-lang.org/book/index.html).

## Какой IDE пользоваться для Rust?

Есть 2 варианта: 

1) Любимый редактор + [RLS](https://github.com/rust-lang/rls):
   преимущества: 
    - не нужно учить другой редактор
    - RLS официальный проект от разработчиков языка
    - RLS использует парсер компилятора
    - RLS работает по Language Server Protocol, который поддерживается большинством современных редакторов

   недостатки:
    - на данный момент RLS не очень стабилен и не всегда правильно работает
    - нетривиальная настройка в некоторых редакторах

2) [IntelliJ Rust](https://intellij-rust.github.io):
   недостатки:
    - потребление ресурсов
    - неполная поддержка языка

   преимещуства:
    - собственный парсер специально заточенный для IDE
    - использует инфраструктуру IntelliJ IDEA
    - знаком пользователям IDEA, CLion, Rider и тд 
    - разработчик плагина сидит в чате, можно сообщать о проблемах

## Как дебажить Rust?

Любой дебаггер для C/C++ работает с Rust. В CLion есть поддержка дебаггера в GUI.

## А кто-нибудь пользуется Rust в продакшене?

Да, вот [список пользователей](https://www.rust-lang.org/production/users).

## А вакансии по Rust есть?

Да, есть, хотя и не много. [Чат для обсуждения вакансий](https://t.me/rust_jobs)

## Не могу установить rustfmt, clippy на rust 1.31

```
rustup self update
rustup toolchain uninstall stable
rustup toolchain install stable
```
