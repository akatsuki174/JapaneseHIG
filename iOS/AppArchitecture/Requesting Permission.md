翻訳元：[Requesting Permission](https://developer.apple.com/design/human-interface-guidelines/ios/app-architecture/requesting-permission/)

# 権限リクエスト

ユーザは現在地、カレンダー、連絡先、リマインダー、写真などの個人情報にアプリがアクセスすることを許可する必要があります。ユーザはこれらの情報にアクセスするアプリの利便性を高く評価する一方で、個人情報をコントロール下におけることも期待しています。例えば、写真に自分の位置情報を自動でタグ付けしたり、近くの友達を見つけたりできるのを良いと思う反面、そのような機能を無効にするオプションも欲しいと考えています。

[スクショ]

**アプリが明らかに必要としている場合のみ、個人情報を要求するようにしましょう。** 明白な理由がない場合は、個人情報を要求することに疑いを持たれるのは当然のことです。明らかに個人情報が必要な機能を使う場合のみ、権限リクエストを行ってください。例えば、現在地の追跡機能を有効にしている時のみ現在地へのアクセスを要求するなどです。

[スクショ]

**アプリが情報を必要とする理由を説明しましょう。** システムの許諾アラートにカスタムテキスト（目的や説明を書いたテキスト）を提供したり、例を含めたりしましょう。テキストは短く具体的にすること、センテンスケースを使用すること、ユーザがプレッシャーを感じないように丁寧にすることを心がけましょう。システム側ですでにアプリを認識しているため、アプリ名を含める必要はありません。開発者向けガイダンスは[Protecting the User's Privacy](https://developer.apple.com/documentation/uikit/core_app/protecting_the_user_s_privacy)をご覧ください。

[図]

**アプリを機能させるために必要な場合のみ、起動時に権限のリクエストをしてください。** アプリの操作が個人情報ありきであることが明らかな場合は、ユーザは権限要求を迷惑がらないでしょう。

**不必要に位置情報を要求しないでください。** 位置情報にアクセスする前に、システム側に位置情報サービスが有効になっているか確認してください。この知識があれば、本当に位置情報が必要な機能に触れるまでアラートを遅らせたり、アラートを完全に避けることができます。位置情報機能の実装方法は[MapKit](https://developer.apple.com/documentation/mapkit)、[Location and Maps Programming Guide](https://developer.apple.com/library/content/documentation/UserExperience/Conceptual/LocationAwarenessPG/Introduction/Introduction.html)をご覧ください。

**システムが提供しているアラートを使いましょう。** 標準の許諾アラートのテキストはカスタマイズできますが、動作や外観を似せたカスタムアラートは避けてください。