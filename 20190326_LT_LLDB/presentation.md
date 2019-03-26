# LLDB custom command

## @takecian

---

# 今日は

* LLDB

---

# Custome command

- 自分でコマンドを作ることができる

---

# 普段 lldb でどんなことやってる？

```
po String(data: data, encoding: .utf8)
```

---

# やり方

- Python でコマンドを書きます
- .lldbinit ファイルをホームディレクトリ下に起きます
- .lldbinit で Python を読み込みます
- Xcode を起動します

---

# Python でコマンドを書きます

読み込まれた時に実行される関数でコマンドを登録する

```python
def __lldb_init_module(debugger,internal_dict):
    debugger.HandleCommand("command script add -f d2s.process d2s")
```

---
# Python でコマンドを書きます

実行したい内容を書く

```python
import lldb

def process(debugger, command, result, internal_dict):
    lldb.debugger.HandleCommand("""
    expr -l swift --
    func $process(_ data: Data) {
        print(String(data: data, encoding: .utf8) ?? "data is nil")
    }
    """.strip())
    lldb.debugger.HandleCommand('expr -l swift -- $process(' + command + ')')

```
---

# .lldbinit

* LLDB起動時に読み込まれるファイル
* この中で Python ファイルを読み込む

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
