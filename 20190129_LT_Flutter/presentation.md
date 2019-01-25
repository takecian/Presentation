# Add flutter to existing app

## @takecian

---

# 今日は

* 既存の iOS アプリに flutter を組み込む話をします

---

# Flutter

* allows you to build beautiful native apps on iOS and Android from a single codebase
  * made by Google
  * Dart
* 流行るかどうかは分からない

---

# Flutter

* Native 側から見ると、一つの ViewController 上で色々やっているように見える
  * FlutterViewController

---

# やり方

1. Create a Flutter module
2. Add your Flutter app to your Podfile
3. Present FlutterViewController

https://github.com/flutter/flutter/wiki/Add-Flutter-to-existing-apps

---

# Native <-> flutter 間の連携
* Platform Channel
  * https://flutter.io/docs/development/platform-integration/platform-channels


![right](https://flutter.io/images/PlatformChannels.png)

---

# Platform Channel

## Method Channel
* メッセージを送った後、結果を受け取れる
* flutter 側から Platform 特有の情報（バッテリー残量取得とか）を取得する時とかに使う

## Event Channel
* 何か状態変化が起きたときの通知用（今回は出てこない）

---
# サンプル
* Native の ViewController から Flutter の画面を呼び出す
* Flutter から Native 側を呼び出して値を取得する
* Flutter 側の画面を切り替える

---

# サンプルコード
* https://github.com/flutter/flutter/wiki/Add-Flutter-to-existing-apps

---
# 終わり