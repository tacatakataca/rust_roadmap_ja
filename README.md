# Rustのチュートリアルマップ
(Mac OS X 10.11.6 El Capitan)  
in 2016.Oct.9(Sun)  

# Rustとは
## Rust
`Rustは、セグメンテーション違反を防ぐ、スレッドセーフティを保証した、超はやい システムプログラミング言語です。`  
[Rust Programming Language](https://www.rust-lang.org/en-US/)

## 速度の話
-[20の言語/環境でてきとうにベンチマークしてみた (Rust, Go, Crystal, Nim, Swiftなど)](http://safx-dev.blogspot.jp/2015/11/20-rust-go-crystal-nim-swift.html)  
-[【まとめ】フィボナッチ数だけで40以上のプログラム言語に精通したつもりになる](http://qiita.com/y_irabu/items/604b0987aa7c8ec52c65#%E5%AE%9F%E8%A1%8C%E9%80%9F%E5%BA%A6%E6%AF%94%E8%BC%83)  
  
とか見たけど、参考程度に。  

## 競合
今からシステム構築する場合、個人的には、Ocaml、Nim、Java、C系(C,C++,C#)、Dあたりが競合かも。  
FortlanとかElangとかあたりははやいと思いますが、不明ですごめんなさい。  
歴代ライブラリ使える点では、Javaとかにはかなわないけど、とにかく書きやすそうみある　　
C系は、Rustから吐けるはず。特に比較対象にならない？  
あと正直、Nimが安定したら、移行検討もありかもわかんない。  

# チュートリアルサイトまとめ
## 総合チュートリアル
- [公式のチュートリアル（日本語訳）]
(https://rust-lang-ja.github.io/the-rust-programming-language-ja/1.6/book/README.html)
- [Rustの動くサンプル集(Rust by Example)（日本語訳）]
(https://github.com/rust-lang-ja/rust-by-example-ja)

# インストール
Rustは↓これでインストールする。  
（厳密には、Rustupをインストールして、そのRustupからインストールしている。）  
`curl https://sh.rustup.rs -sSf | sh`  
[Rustup](https://www.rustup.rs/)  
[Rustupの説明](https://blog.rust-lang.org/2016/05/13/rustup.html)
## Rustup
Rustupとは、rubenv,pyenvみたいなやつ。ツールチェーンのインストール、バージョン管理できるやつ。  
nightlyを使うが吉。  
[std](https://doc.rust-lang.org/beta/std/)は[標準ライブラリ](https://doc.rust-lang.org/beta/std/)のこと。  
[rustc](https://manishearth.github.io/rust-internals-docs/rustc/)はコンパイラのこと。　　
[cargo](#)はプロジェクト管理系？  

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
[こういうの](http://stackoverflow.com/questions/27269315/how-do-i-debug-a-failing-cargo-test-in-gdb)を参考に。  

# ライブラリまとめ
## std
[std](https://doc.rust-lang.org/beta/std/)

## 機械学習系
-[機械学習コミュニティ紹介記事](https://medium.com/@autumn_eng/about-rust-s-machine-learning-community-4cda5ec8a790#.4nxykw8ul)  
記事紹介している団体自体は、RustのGPU関連アロックのライブラリ公開しているっぽい？  

# 開発環境まとめ
## IntelliJ
[Jetbrains IntelliJ](https://www.jetbrains.com/)  
-IntelliJ Rust Plugin
## Emacs
`rust-mode`,`flycなんたらrust`


# 気になってることたち
## コマンド関連
-[cargo withオプション](https://github.com/rust-lang/cargo/pull/1763)  
stableじゃ入ってないのかな。
