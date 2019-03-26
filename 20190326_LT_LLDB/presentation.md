# LLDB custom command

## @takecian

---

# 今日は

* LLDB

---

# Custome command

- 自分でコマンドを作ることができる

---

# やり方

- python でコマンドを書きます
- .lldbinit ファイルをホームディレクトリ下に起きます
- .lldbinit で python を読み込みます
- Xcode を起動します

---

# python でコマンドを書きます

読み込まれた時に実行される関数でコマンドを登録する

```
def __lldb_init_module(debugger,internal_dict):
```

---

# .lldbinit

* LLDB起動時に読み込まれるファイル
* この中で python ファイルを読み込む

---

# 普段 lldb でどんなことやってる？

```
po String(data: data, encoding: .utf8)
```

---

# 登録してみた

デモ

---

# 便利なのあった

facebook が作ってる Custom command 集
https://github.com/facebook/chisel

---

# 色々便利なコマンドがあった

hide/show
mask/unmask

---

# 参考

- https://developer.apple.com/videos/play/wwdc2018/412/
- https://github.com/facebook/chisel
