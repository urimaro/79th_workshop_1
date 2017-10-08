## Making Ruby?
## ゆるふわRuby生活

パッチモンスターこと中田さん

---

笹田さんがcookpadに移籍したので、  
事務処理できる人がいなくなったとのこと

---

### 概要

- 1. Rubyの開発について
  - A. リポジトリ
  - B. 新機能/課題の管理
  - C. 開発者会議
- 2. Rubyのビルドの仕方
- 3. バグ事例
- 4. Ruby2.5について

---

### 1. Rubyの開発環境について

---

### A. リポジトリ

- Subversionで管理している
- GitHubにミラーがある

---

よくある質問

---

Q. なぜGitを使わないのか？

---

### 1. RubyはGitより古い

- Ruby: 1993  
- Git: 2005

---

### 2. hashがわかりにくい

- commit id(hash)  
    コミットごとにhashが割当てられる
- revision number  
    ソース全体に同じ番号が割当てられる

---

### 3. 公式にはwindowsをサポートしていない

---

**コミッターにメリットない**

---

### 新機能/課題の管理

---

Redmineで管理している

---

### 開発者会議

---

月に1回開催している

---

### Rubyのビルドの仕方

1. tar ballを使う
2. リポジトリのソースコードを使う

---

### 1. tar ballを使う

tar ball + configure + makeコマンド

---

### 2. リポジトリのソースコードを使う

リポジトリからRubyをビルドするのは  
手間がかかる

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

処理の並列化など  
ビルドプロセスの改善中

---

### バグフィックスの事例

---

**Rubyは「簡単な文法」だと「錯覚」させている**

---

### 1. 変数pとpメソッド

---

### 2. String#internをrefinementsすると式展開された文字列からsymbolが作られない  

---

- String#intern: 文字列に対応するsymbolを返す
- Refinements: クラスの拡張範囲を限定する機能

---

↓が文字列になってしまう

```
:"#{foo}"
```

らしい

---

### Ruby2.5について

---

**No eye-catcher feature in 2.5**

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

**もっと「Rubyを」いじってね**

ということだと思いました。

---

Rubyのなかを覗いてみよう！  
「Cookpad Ruby Hack Challenge」に参加してみた  
池澤あやかさん  
https://codeiq.jp/magazine/2017/09/53932/


Cookpad Ruby Hack Challenge - 笹田さん  
https://github.com/ko1/rubyhackchallenge
