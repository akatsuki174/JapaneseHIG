翻訳元：[Navigation](https://developer.apple.com/design/human-interface-guidelines/ios/app-architecture/navigation/)

# ナビゲーション

人はアプリのナビゲーションが期待に沿わないと気づかない傾向があります。あなたがやることは、アプリの構造と目的に合った方法でナビゲーションを実装しつつ、それ自体には目を奪われない状態にすることです。ナビゲーションは自然で親しみやすくあるべきで、インターフェースを掌握したり、コンテンツから目をそらさせるものであってはいけません。iOSのナビゲーションには主に3つのスタイルがあります。

## 階層型ナビゲーション

目的地にたどり着くまで1画面につき1つ選択をします。別の目的地に行くには手順をやり直すか、最初に戻って別の選択をする必要があります。設定アプリとメールアプリはこのナビゲーションスタイルを使用しています。

[図]

## フラットナビゲーション

複数のコンテンツカテゴリを切り替えます。音楽アプリ、App Storeアプリはこのナビゲーションスタイルを使用しています。

[図]

## コンテンツ駆動、体験駆動ナビゲーション

コンテンツ内を自由に移動したり、コンテンツ自体がナビゲーションを定義したりします。ゲームアプリ、Booksアプリ、その他没入型アプリは一般的にこのナビゲーションスタイルを使用しています。

[図]

アプリの中には複数のナビゲーションスタイルを組み合わせているものもあります。例えばフラットナビゲーションを使用しているアプリが各カテゴリ内に階層型ナビゲーションを実装することもあります。

**常に明確なパスを示してください。** ユーザは今アプリのどこにいるのか、どうやったら次の目的地に辿り着けるのかを常に知っている必要があります。ナビゲーションスタイルに限らず、コンテンツへのパスは論理的に筋が通っていること、予測可能なこと、辿りやすいことが大切です。基本的には、各画面へのパスは1つにします。もし1つの画面を複数のコンテキストで見る必要がある場合は、アクションシート、アラート、ポップアップ、モーダルビューの使用を検討してください。より詳しく知りたい場合は、[Action Sheets](https://developer.apple.com/design/human-interface-guidelines/ios/views/action-sheets/)、[Alerts](https://developer.apple.com/design/human-interface-guidelines/ios/views/alerts/)、[Popovers](https://developer.apple.com/design/human-interface-guidelines/ios/views/popovers/)、[Modality](https://developer.apple.com/design/human-interface-guidelines/ios/app-architecture/modality/)をご覧ください。

**コンテンツに素早く、簡単に辿り着けるような情報構造設計をしましょう。** 最低限のタップ数、スワイプ数、画面数で済むような情報構造を作り上げましょう。

**移動しやすさのためにタッチジェスチャーを使いましょう。** 触れるのを最小限に抑えて、インターフェース上の移動を楽にしましょう。例えば前の画面に戻るのに画面の横からスワイプするなどです。

**標準のナビゲーションコンポーネントを使用しましょう。** 可能な限り、ページコントロール、タブバー、セグメンティッドコントロール、テーブルビュー、コレクションビュー、スプリットビューなどの標準的なナビゲーションコントロールを使用しましょう。ユーザはこれらのコントロールにはすでに慣れているので、アプリ内の移動方法を直感的に知ることができます。

**ナビゲーションバーを使用してデータの階層を辿れるようにしましょう。** ナビゲーションバータイトルは階層内の現在の位置を表示することができますし、戻るボタンは前の画面に簡単に戻ることができます。具体的なガイダンスは[Navigation Bars](https://developer.apple.com/design/human-interface-guidelines/ios/bars/navigation-bars/)を参照してください。

**タブバーを使用して、コンテンツや機能的に同じカテゴリを表示しましょう。** タブバーを使用すると、現在の位置に関係なく素早く簡単にカテゴリを切り替えることができます。詳細は[Tab Bars](https://developer.apple.com/design/human-interface-guidelines/ios/bars/tab-bars/)をご覧ください。

**同じタイプのコンテンツが複数ページある場合は、ページコントロールを使用しましょう。** ページコントロールは利用可能なページ数や現在アクティブなページをはっきり伝えることができます。天気アプリではページコントロールを使用して場所ごとの天気ページを表示しています。より詳しいガイダンスは[Page Controls](https://developer.apple.com/design/human-interface-guidelines/ios/controls/page-controls/)をご覧ください。


ヒント  
セグメンティッドコントロールとツールバーではナビゲーションはできません。情報を異なるカテゴリに整理するときに異なるカテゴリにセグメンティッドコントロールを使います。ツールバーは現在のコンテキストに対してインタラクティブに操作するときに使います。これらのタイプの要素について詳しく知りたい方は、[Segmented Controls](https://developer.apple.com/design/human-interface-guidelines/ios/controls/segmented-controls/)、[Toolbars](https://developer.apple.com/design/human-interface-guidelines/ios/bars/toolbars/)をご覧ください。