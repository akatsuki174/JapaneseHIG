翻訳元：[User Interaction](https://developer.apple.com/design/human-interface-guidelines/accessibility/overview/user-interaction/)

# ユーザインタラクション

VoiceOver のような支援技術やディスプレイ調節などのアクセシビリティ機能により、人々がデバイスを操作する方法が広がってきています。これらの技術や機能はシステムが提供するインタラクションと一体化しているため、それを正しくサポートすることが重要になってきます。

# ジェスチャー

**すべてのコントロールとインタラクティブ要素に、少なくとも 44pt x 44pt のタップ領域を与えましょう。**動きが制限されているユーザでもアプリ操作をしやすい状態にするためには、より大きなタップ領域が必要になります。コントロールが小さすぎるとすべてのユーザにとってタップがしづらく、イライラさせてしまうことになります。

**プラットフォームで定義されているジェスチャーをオーバーライドしないようにしましょう。**ユーザは使用しているアプリに関係なく、スワイプダウンしたら通知センターが確認できたり、macOS のシステム設定のトラックパッドジェスチャーで設定したシステムジェスチャーが機能することを期待しています。

**インタラクションにはシンプルなジェスチャーを。**マルチフィンガージェスチャーやロングプレス、複数回ボタンをタップするなどの複雑なジェスチャーは、多くの人にとって困難な可能性があります。可能な限りシンプルなジェスチャーにすると、アプリを使う全てのユーザの体験が向上します。

**ジェスチャーベースのアクションの代替手段を提供しましょう。**特定のジェスチャーを実行できない可能性のある人向けにオプションを用意しましょう。例えばスワイプでテーブル要素を削除する場合、編集モードやアイテム詳細画面での削除ボタンなどの代替手段を提供する必要があります。

**iOS アプリでドラッグ&ドロップができるようにしましょう。**アクセシビリティ API を使用してアプリ内のドラッグ元とドロップ先を指定すると、画面上のアイテムをドラッグ&ドロップできるようになります。詳しくは[accessibilityDragSourceDescriptors](https://developer.apple.com/documentation/objectivec/nsobject/2891001-accessibilitydragsourcedescripto)や[accessibilityDropPointDescriptors](https://developer.apple.com/documentation/objectivec/nsobject/2891048-accessibilitydroppointdescriptor)などの開発者向けガイドラインを見ましょう。

**iOS の 3D タッチや Apple Watch のフォースタッチなしでコア機能を使えるようにしましょう。**誰もが画面を押して 3D タッチやフォースタッチで提供されている追加機能を利用できるわけではありません。3D タッチやフォースタッチが利用できない場合でもすべてのユーザがアプリの重要なアクションを実行できるようにしましょう。

ジェスチャーについてより多くのことを学びたい場合は、[Clicks and Gestures (macOS)](https://developer.apple.com/design/human-interface-guidelines/macos/user-interaction/mouse-and-trackpad/#clicks-and-gestures/)、[Gestures (tvOS)](https://developer.apple.com/design/human-interface-guidelines/tvos/remote-and-controllers/remote/#gestures)、[Gestures (watchOS)](https://developer.apple.com/design/human-interface-guidelines/watchos/user-interaction/gestures/)、[Gestures (iOS)](https://developer.apple.com/design/human-interface-guidelines/ios/user-interaction/gestures/)を御覧ください。

# Haptics

**システムで定義されているhapticsをサポートしましょう。**多くの人は画面が見えない時にアプリを操作する場合、触覚に頼っています。例えばシステムアプリはタスクが成功、失敗した時やイベントが発生しようとしている時、それをhapticsを使ってユーザに伝えます。ユーザが混乱しないよう、システム定義されたhapticsを使用するようにしてください。

システム定義されたhapticsについてより知りたい場合は、[Haptic Feedback (macOS)](https://developer.apple.com/design/human-interface-guidelines/macos/user-interaction/mouse-and-trackpad/#haptic-feedback)、[Haptics (iOS)](https://developer.apple.com/design/human-interface-guidelines/ios/user-interaction/haptics/)、[Haptic Feedback (watchOS)](https://developer.apple.com/design/human-interface-guidelines/watchos/user-interaction/haptic-feedback/)を参照してください。

# ボタンとコントロール

**カスタム要素のアクセシビリティはそれが何であるかわかるようにしましょう。** UIKit の accessibility traits と AppKit の properties を使用すれば、ある要素の振る舞いをアクセシビリティ支援技術に伝えることができます。例えば [button](https://developer.apple.com/documentation/uikit/uiaccessibility/uiaccessibilitytraits/1620194-button)、もしくは [NSAccessibilityButton](https://developer.apple.com/documentation/appkit/nsaccessibilitybutton) を使用して view を button として認識させると、VoiceOver はビューの説明に続いて *button* という単語を読み上げ、 view が button のように振る舞うことを伝えられます。

**一貫したスタイル階層を使用して、ボタンの相対的な重要性を伝えるようにしましょう。**ボタンシェイプを有効にすると、アクティブなボタンとそれを囲むコンテンツとの境が見分けやすくなります。一貫したボタンスタイル階層を使用すれば、見た目からボタンの重要性を把握することができます。例えば最も重要なボタンは角丸長方形で色が塗りつぶされているもの、次に重要なボタンは色こそ塗りつぶされていないものの、テキストかグリフがキーカラーで塗られているもの、最も重要度の低いボタンは下線付きテキストというような具合です。

**システムが提供しているスイッチを使うようにしましょう。** UIKit が提供するスイッチは、ノブの位置と色で状態を表しています。一部の人にとってはラベルを付け加えることでよりスイッチがオンなのかオフなのかがわかりやすくなります。システムが提供しているスイッチを使うと、スイッチのオンオフを切り替えた時に iOS が自動的にグリフ内にオンオフを表示してくれます。

**リンクに下線などの視覚的な目印を付けることを検討しましょう。**色を使ってリンクであることを示すのは構いませんが、それを唯一の目印として使用すると、色覚障害を持つ人にとっては違いが区別できない可能性があります。色によるコミュニケーションについてもっと知りたい場合は[Color and Contrast](https://developer.apple.com/design/human-interface-guidelines/accessibility/overview/color-and-contrast/)を参照してください。

# ユーザ入力

**タイピングの代わりに音声で情報を入力できるようにしましょう。**テキスト入力フィールドにディクテーションボタンを追加すると、人々は好みの入力方法として音声を選択することができます。もしカスタムキーボードを作るのであれば、ディクテーション用のマイクキーを含めるようにしてください。

**音声のみで重要なタスクを実行できるよう、Siri や Siri ショートカットのサポートをしてください。**アプリで Siri を活用するための方法については [SiriKit](https://developer.apple.com/design/human-interface-guidelines/sirikit/) を参照してください。

**ユーザがプレーンテキストを選択するのを妨げないようにしてください。**多くのユーザはテキスト読み上げ（TTS）や翻訳の検索入力のためにテキスト選択機能に頼っています。
