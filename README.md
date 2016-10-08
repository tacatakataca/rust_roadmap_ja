# Rust言語のチュートリアルマップ
(Mac OS X 10.11.6 El Capitan)  
in 2016.Oct.9(Sun)  
まだ途中だけど大体こんな感じ？

# チュートリアルサイトまとめ
## 総合チュートリアル
- 公式のチュートリアル（日本語訳）
https://rust-lang-ja.github.io/the-rust-programming-language-ja/1.6/book/README.html
- 動く Rust Example（日本語訳）
https://github.com/rust-lang-ja/rust-by-example-ja

# インストール
Rustは↓これでインストールする。  
（厳密には、Rustupをインストールして、そのRustupからインストールしている。）  
`curl https://sh.rustup.rs -sSf | sh`  
by https://www.rustup.rs/  
## Rustup
Rustupとは、rubenv,pyenvみたいなやつ。ツールチェーンのインストール、バージョン管理できるやつ。  
nightlyを使うが吉。  
stdは何？  
rustcはコンパイラ？  
cargoはプロジェクト管理系？  

## プロジェクト作成方法（なげやり）
`cargo --help`ででる。  
現在ディレクトリをプロジェクトに：`cargo init`  
ディレクトリと一緒にプロジェクト作成：`cargo new PROJECT_NAME`  

## 実行（rustcを使った方法　）
`rustc NAME.rs`
`./NAME`

## 実行（cargoでプロジェクトを作った場合　）
`cargo run`

## ビルド（cargoでプロジェクトを作った場合　）
`cargo build`

## デバッグ
### ビルド時にデバッグ
`cargo build`
一緒にデバグされる。  
もっと深く行きたいなら、`test`オプションを使う。

### GDBを使ったデバッグ
`$ gdb target/debug/PROJECT_NAME`
`$(gdb) break rust_panic`
`$(gdb) run --test test_extract_failure`
とか。  
こういうのを参考に。  
http://stackoverflow.com/questions/27269315/how-do-i-debug-a-failing-cargo-test-in-gdb

# 開発環境まとめ
## IntelliJ
Jetbrains IntelliJ https://www.jetbrains.com/  
-IntelliJ Rust Plugin
## Emacs
`rust-mode`,`flycなんたらrust`

