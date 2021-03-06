翻訳元：[Buttons](https://developer.apple.com/design/human-interface-guidelines/ios/controls/buttons/)

# ボタン

ボタンはアクションをスタートさせるものであり、カスタマイズ可能な背景を持っていたり、タイトル、アイコンを含んでいたりします。ほとんどのユースケースをカバーできるよう、システム側で予め定義したボタンはいくつかあります。また、完全に自分でカスタマイズしたボタンを作ることもできます。

開発者向けガイダンスは[UIButton](https://developer.apple.com/documentation/uikit/uibutton)を見てください。

## システム定義のボタン

システムが用意しているボタンはナビゲーションバーやツールバーによくありますが、これはどこでも使用することができます。

[画像]

**タイトルには動詞を使いましょう**

アクションボタンのタイトルはインタラクティブで、タップした時に何が起こるのかわかるようなものであるべきです。

**タイトルにはタイトルケースを使いましょう**

冠詞、等位接続詞、4文字以下の前置詞を除いて、全ての語を大文字にしましょう。

**タイトルは短くしましょう**

テキストが長いとインターフェースは煩雑になりますし、小さい画面ではカットされてしまいます。

**必要な時のみ、ボーダーや背景を入れることを検討してください**

デフォルトではシステム標準のボタンにボーダー、背景はありません。しかし場合によってはボーダーや背景が必要になってきます。電話アプリではボーダーで囲まれた数字キーが伝統的な電話のイメージを強めてますし、電話をかけるボタンの背景色は目に付きやすいようになっています。

開発者向けガイダンスは[UIButton](https://developer.apple.com/documentation/uikit/uibutton)の[UIButtonTypeSystem](https://developer.apple.com/documentation/uikit/uibuttontype/uibuttontypesystem)を見てください。

## 詳細表示ボタン

詳細表示ボタンは、追加情報や画面上の特定の項目に関連する機能について書かれたビュー（通常はモーダルビュー）を表示します。詳細表示ボタンはどんなタイプのビューにでも使うことができますが、普通はテーブルの中で特定の行の情報にアクセスするために使われます。

[写真]

**詳細表示ボタンはテーブルの中で適切に使いましょう**

テーブル行内に詳細表示ボタンがある場合、タップすると追加情報が表示されます。その他の部分をタップすると行が選択されるかアプリで定義された動作が実行されます。もし追加情報を見るのに行全体をタップしてほしい場合は、詳細表示ボタンを使わないでください。代わりにシェブロン（＞）のように見える詳細表示アクセサリーコントロールを使ってください。詳しくは[UITableViewCell](https://developer.apple.com/documentation/uikit/uitableviewcell)の[UITableViewCellAccessoryType](https://developer.apple.com/documentation/uikit/uitableviewcellaccessorytype)を見てください。

開発者向けガイダンスは[UIButton](https://developer.apple.com/documentation/uikit/uibutton)の[UIButtonTypeDetailDisclosure](https://developer.apple.com/documentation/uikit/uibuttontype/uibuttontypedetaildisclosure)を見てください。

## インフォボタン

インフォボタンはアプリの詳細を表示します。場合によってはビューが回転して表示されることもあります。このボタンはlightとdarkの2つのスタイルがあります。自分のアプリのデザインに最も合ったスタイルを選択し、画面に埋もれないようにしてください。

開発者向けガイダンスは[UIButton](https://developer.apple.com/documentation/uikit/uibutton)の[UIButtonTypeInfoLight](https://developer.apple.com/documentation/uikit/uibuttontype/uibuttontypeinfolight)と[UIButtonTypeInfoDark](https://developer.apple.com/documentation/uikit/uibuttontype/uibuttontypeinfodark)を見てください。

## 連絡先追加ボタン

既存の連絡先リストを見てテキストフィールドや他のビューに追加したい時、このボタンをタップします。例えばメールではメッセージの宛先フィールドにある連絡先追加ボタンをタップすると連絡先リストから受信者を選択できます。

[写真]

**連絡先追加ボタンに加えてキーボード入力も使えるようにしておきましょう**

連絡先追加ボタンは連絡先情報を入力する時の唯一の手段ではなく選択肢です。このボタンは既存の連絡先から追加するためのショートカットとして提供し、キーボードでも連絡先情報を入力できるようにするのが良いです。

開発者向けガイダンスは[UIButton](https://developer.apple.com/documentation/uikit/uibutton)の[UIButtonTypeContactAdd](https://developer.apple.com/documentation/uikit/uibuttontype/uibuttontypecontactadd)を見てください。