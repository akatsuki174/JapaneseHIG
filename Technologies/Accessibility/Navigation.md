翻訳元：[Navigation](https://developer.apple.com/design/human-interface-guidelines/accessibility/overview/navigation/)

# ナビゲーション

**プラットフォームの標準と辻褄の合う、予測可能で論理的なナビゲーションをデザインしましょう。**ユーザがシステムアプリや他のアプリを使ったときの体験を活用できるなら、アプリの操作法を覚えるのはかなり簡単になります。アプリナビゲーションの標準的なスタイルについては [Navigation (iOS)](https://developer.apple.com/design/human-interface-guidelines/ios/app-architecture/navigation/)、[Navigation (watchOS)](https://developer.apple.com/design/human-interface-guidelines/watchos/app-architecture/navigation/)、[Navigation (tvOS)](https://developer.apple.com/design/human-interface-guidelines/tvos/app-architecture/navigation/)を御覧ください。

# ナビゲーションと VoiceOver

**VoiceOver ですべての要素の案内が可能になっているか確認してください。** VoiceOver は画面上のアクセシビリティ情報を使って各要素がどこにあるのか、それを使って何ができるのかをユーザが理解できるようにします。システムが提供する UI 要素にはデフォルトでこのアクセシビリティ情報が含まれています。しかしこちらから情報を提供しない限り、 VoiceOver はカスタム要素を見つけたり使用したりする手助けを行うことはできません。

**要素をグループ化、整列化、リンク化して、VoiceOver 体験を向上させましょう。**proximity、alignment やその他コンテキスト把握の手がかりになるようなものは、目の見えるユーザにとっては要素間の関係性を理解するのに役立ちますが、VoiceOver ユーザにとってはその限りではありません。目の見えるユーザのみが要素間の関係性を理解できる場所を把握し、VoiceOver がその関係性を説明できるようにしましょう。

例えば次のレイアウトは要素間の近さとセンタリングによって、各フレーズが画像のキャプションであるということを示しています。しかし各画像とフレーズをグルーピングするよう VoiceOver に伝えていないと、VoiceOver は "A large container holding a variety of mangoes. 
A large container holding many green artichokes. 
Mangoes come from trees that belong to the genus Mangifera. 
Artichokes come from a variety of a species of thistle." と読んでしまいます。これは、デフォルトでは VoiceOver は要素を左から右に読むために発生します。

コントロールを紹介するテキストは、目が見えるユーザにとっては理解を助ける視覚的手がかりになります。以下に示す例では VoiceOver ユーザがこのコントロールを理解できるように、"Default web browser:" がポップアップボタンのラベルであることを、システム環境設定が VoiceOver に伝えています。

開発者向けガイダンスは [shouldGroupAccessibilityChildren](https://developer.apple.com/documentation/objectivec/nsobject/1615143-shouldgroupaccessibilitychildren) と [accessibilityTitleUIElement](https://developer.apple.com/documentation/appkit/nsaccessibility/1535155-accessibilitytitleuielement?language=occ) を御覧ください。

**画面上のコンテンツやレイアウトが変わったら、VoiceOver に教えてあげましょう。**予期せぬコンテンツやレイアウトの変更は、VoiceOver ユーザをとても混乱させます。これは頭で思い描いた画面マップがもはや正しくないことを意味します。画面上の変更を VoiceOver や他のアクセシビリティ支援技術が解釈してユーザに伝えられるよう、きちんと伝えることが重要です。

**異なるwebページやアプリを開くコントロールをアクティブにする前に、注意書きを出しましょう。**特に注意がなくコンテキストが変わると混乱が生じ、急いで頭の中の画面モデルを再構築しなければならなくなります。

**すべての重要なインターフェース要素に代替テキストラベルを提供しましょう。**代替テキストラベルは画面上には表示されませんが、VoiceOver が画面上の要素を音声で説明してくれるため、視覚障害を持つ人をナビゲートするのが容易になります。システム提供のコントロールはデフォルトで便利なラベルが付いていますが、カスタムラベルの場合は自分で作る必要があります。例えば自作の評価ボタンのアクセシビリティ要素を作成する場合は、ラベルとして"Rate."を指定するなどです。

**VoiceOverロータをサポートしましょう。** VoiceOver ユーザは、ドキュメントや web ページの見出し、リンク、その他セクションタイプを案内できるロータという画面上のコントロールを使用します。このロータは点字キーボードも表示できます。ロータにこれらのアイテムが識別できるようにすることで、VoiceOver ユーザをアプリ内の関連アイテムに案内することができます。開発者向けガイダンスは [UIAccessibilityCustomRotor](https://developer.apple.com/documentation/uikit/uiaccessibilitycustomrotor)、 [NSAccessibilityCustomRotor](https://developer.apple.com/documentation/appkit/nsaccessibilitycustomrotor) を御覧ください。

**キーボードを使用して、macOS アプリの画面上にあるすべての要素を操作できるようにしましょう。**理想としてはユーザがフルキーボードアクセスを有効にし、キーボードのみを使用して macOS アプリのすべてのタスクを実行できる状態だと良いです。macOS ではアクセシビリティキーボードショートカットに加えて、多くの人が普段使う他のキーボードショートカットについても定義しています。すべてのユーザーをサポートするには、アプリ側でキーボードショートカットを上書きしないようにすることが重要です。
