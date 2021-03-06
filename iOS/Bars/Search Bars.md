翻訳元：[Search Bars](https://developer.apple.com/design/human-interface-guidelines/ios/bars/search-bars/)

# 検索バー

検索バーを使用すると、フィールドにテキストを入力することで大量のコレクションから検索することができます。検索バーは単独で表示することも、ナビゲーションバーの中やコンテンツビューの中に表示することもできます。検索バーをナビゲーションバーの中に表示する場合、いつでも利用しやすいようにナビゲーションバーに固定して表示したり、ユーザが下にスワイプして表示させようとするまで隠しておくこともできます。

[スクショ]

**検索機能はテキストフィールドではなく検索バーを使用してください。** テキストフィールドは、人々が期待するような標準的な検索バーの見た目ではありません。

**クリアボタンを有効にしてください。** 多くの検索バーはフィールドの内容を消せるクリアボタンがあります。

**必要に応じてキャンセルボタンを有効にしてください。** 多くの専用検索バーには、すぐに検索を終了するキャンセルボタンがあります。

[スクショ]

**必要であれば、検索バー内にヒントやコンテキストを表示してください。** 検索バーフィールドは、検索のコンテキストを思い出せるようにするために「Search Clothing, Shoes and Accessories」のようなプレースホルダーや単に「Search」のようなテキストを含めることができます。また、簡潔に、句読点を含めつつ1行で記述したプロンプトを、検索バーのすぐ上に表示してガイダンスを提供することもできます。株価アプリでは会社名や株式記号を入力することができることを知らせるためにプロンプトを使っています。

[スクショ]

**検索バーの下に役立つショートカットやその他のコンテンツを提供することを検討してください。** 検索バーの下の領域を使うことによって人々がより早くコンテンツに辿り着けるようになります。例えばSafariでは検索フィールドをタップするとすぐにブックマークが表示されます。ブックマークを選択すると検索語を入力しなくてもすぐにそのブックマークに移動できます。株価アプリでは検索フィールドに入力するとすぐに結果リストが表示されます。多くの文字を入力しなくても、いつでも1つはタップするものがあります。

開発者向けのガイダンスは[UISearchController](https://developer.apple.com/documentation/uikit/uisearchcontroller)と[UISearchBar](https://developer.apple.com/documentation/uikit/uisearchbar)を御覧ください。

## スコープバー

スコープバーは検索バーに追加することができ、検索範囲の絞り込みに使うことができます。

[スクショ]

**スコープバーを含めるより検索結果を改善するようにしてください。** スコープバーは検索するカテゴリーが明確に定義されている場合には便利です。しかし検索結果を改善して、スコープバーが必要ないようにするのがベストです。

開発者向けのガイダンスは[UISearchBar](https://developer.apple.com/documentation/uikit/uisearchbar)をご覧ください。