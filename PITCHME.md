## Making Ruby? ゆるふわRuby生活

パッチモンスターことナカダさん

---

笹田さんがcookpadに移籍したので、<>
事務処理できる人がいなくなったとのこと

---

#### 概要

- Rubyの開発について
  - リポジトリ
  - 新機能/課題の管理
  - 開発者会議
- Rubyのビルドの仕方
- バグ事例
- Ruby2.5について

---

#### リポジトリ

- Subversinoで管理している
- GitHubにミラーがある

---

よくある質問

---

RubyはSubversionを使って、<br />
ソースコードを管理している

---

なぜGitを使わないのか

---

1. RubyはGitより古い  
    Ruby: 1993  
    Git: 2005

---

2. hashがわかりにくい
    - commit id(hash)  
        コミットごとにhashが割当てられる
    - revision number  
        ソース全体に同じ番号が割当てられる

---

3. 公式にはwindowsをサポートしていない

---

**コミッターにメリットない**

---

#### 新機能/課題の管理

---

Redmineで管理している

---

#### 開発者会議

---

月に1回開催している

---

#### Rubyのビルドの仕方
1. tar ballを使う
2. リポジトリのソースコードを使う

---

#### 1. tar ballを使う
tar ball + configure + makeコマンド

---

#### 2. リポジトリのソースコードを使う
リポジトリからRubyをビルドするのは手間がかかる

---

**RubyをビルドするのにRubyが必要！**

---

- ベースとなるRuby  
    ファイルの変換に使っている

- mini Ruby  
    mini rubyはビルド中に作られる
    Makefile、拡張ライブラリを生成したりする
    debugしやすい

---

処理の並列化などビルドプロセスの改善中

---

#### バグフィックスの事例

---

**Rubyは「簡単な文法」と「錯覚」させている**

---

#### 1. 変数pとpコマンド

---

#### 2. String#internをrefinementsすると式展開された文字列からsymbolが作られない  
文字列になってしまう

- String#intern: 文字列に対応するsymbolを返す
- Refinements: クラスの拡張範囲を限定する機能

---

Ruby2.5: no eye-captcher feature

---

ってこともないよ。

---

- rescue inside do/end
- Array#append, prepend
- Hash#transform_keys
- Kernel#yield_self

---

右代入についても話題になっている

---

#### 感想

---

**もっと「Rubyを」いじってね**<br />
ということだと思いました。

---

Rubyのなかを覗いてみよう！
「Cookpad Ruby Hack Challenge」に参加してみた
池澤あやかさん
https://codeiq.jp/magazine/2017/09/53932/


Cookpad Ruby Hack Challenge - 笹田さん
https://github.com/ko1/rubyhackchallenge
