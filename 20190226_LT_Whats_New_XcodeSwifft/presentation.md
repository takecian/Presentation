# What's new Xcode 10.2 and Swift5

## @takecian

---

# 今日は

* Xcode 10.2 で何が変わるの、という話

---

# 話の前に

Xcode Beta 10.2 をインストールしてください

---

# General
Xcode が macOS content caching サポートした

よくわからない
https://support.apple.com/ja-jp/guide/mac-help/about-content-caching-on-mac-mchl9388ba1b/mac

---
# Interface builder

- ダブルクリックでの拡大縮小がなくなる
- Trackpad でのピンチ・Optionを押しながらのスクロールになる

---

# Source Editor

Computed property の畳み込みができるようになった

Edit -> Code Folding -> Fold Methoods & Functions

---
# Testing
xccov(Xcodeのtest coverage report のやつ)が色々改善されたらしい

- coverage reports の差分が取れるようになった
- 複数のレポートを結合できるようになった

---
# App thinning

配布時のアプリサイズをいい感じにするやつの総称
- Bitcode
- App slicing
- On-Demand Resources (ODR)

https://help.apple.com/xcode/mac/current/#/devbbdc5ce4f

---

# App thinning

これに新しく追加される

- Swift の標準ライブラリのためのdynamic link libraryとSwift SDK overlayがアプリに含まれなくなる
- iOS12.2 から

- つまり？
  - ファイルサイズが小さくなるらしい

---

# ファイルサイズってどこで見るの？

- AppStore Connect -> Activity -> All Builds

---

# Swift 5 変更点

これ clone して試してみましょう
https://github.com/twostraws/whats-new-in-swift-5-0

---

# 参考

https://developer.apple.com/documentation/xcode_release_notes/xcode_10_2_beta_3_release_notes
https://developer.apple.com/documentation/xcode_release_notes/xcode_10_2_beta_3_release_notes/swift_5_release_notes_for_xcode_10_2_beta_3


https://www.hackingwithswift.com/articles/126/whats-new-in-swift-5-0

