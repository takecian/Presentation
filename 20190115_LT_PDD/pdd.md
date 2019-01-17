# Introducing Playground Driven Development

## @takecian

---

## PDD 

---

# PPD

Kickstarter の iOS アプリで採用されている
Xcode Playground で UI の確認をしながら開発する手法

* https://github.com/kickstarter/ios-oss
* https://talk.objc.io/episodes/S01E51-playground-driven-development-at-kickstarter

---

# Xcode Playground

* コードを簡単に動作させられる便利なやつ
* Cocoa touch framework を Playground から呼び出す例@WWDC2018

  * https://developer.apple.com/videos/play/wwdc2018/402/

---

# やり方

1. Xcode Playgronud で使いたい ViewController を Cocoa touch framework で作る
2. Xcode Playgronud から ViewController を呼び出す

![inline](https://camo.qiitausercontent.com/1e94097753dbd4b0c8579bf87f716fe6bd0c702b/68747470733a2f2f71696974612d696d6167652d73746f72652e73332e616d617a6f6e6177732e636f6d2f302f32373231302f39336561356134352d346163642d313630622d663063662d3166366235646139333339382e706e67)

---

# 詳しいやり方はここ

https://qiita.com/takecian/items/1f492e5a12cf3ccdfa77

---

# デモ

---

# 制約

* Xcode playground から Application target のコードは呼び出せない
* Cocoapods のライブラリを使おうとすると魔術が必要
* Cocoa touch framework のコードを変更したら再ビルドが必要
