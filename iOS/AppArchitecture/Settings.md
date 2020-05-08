翻訳元：[Settings](https://developer.apple.com/design/human-interface-guidelines/ios/app-architecture/settings/)

# 設定

一部のアプリはセットアップ、設定を選択する場所を提供する必要があるかもしれませんが、多くのアプリではそうすることを避けたり、遅らせることができます。成功しているアプリは多くの人にとってすぐにちゃんと機能するようになっている一方で、体験を調節するための便利な方法も提供しています。アプリを設計する時は多くの人が期待する方法で機能するようにすると、設定の必要性を減らすことができます。

[スクショ]

**システムから可能な限りのことを推測しましょう。** もしユーザ、デバイス、環境設定に関する情報が必要な場合は、可能な限りユーザに尋ねるのではなく、システムに問い合わせてください。例えば、ローカル情報に基づいた選択肢を表示するために郵便番号を入力させるのではなく、現在地への使用許可を求めるようにしましょう。ユーザが自分の情報へのアクセスを拒否した場合は、潔く手動入力に切り替えましょう。

**アプリ内の設定オプションにはしっかり優先順位を付けてください。** アプリのメイン画面は、必須のオプションや頻繁に変更されるオプションを配置するのに適しています。たまにしか変更されないオプションはその次の画面の方が適しています。

**頻繁に変更されないオプションは設定アプリに並べておきましょう。** 設定アプリはシステム全体を通じて設定変更を行うための中心的な場所ですが、そこにたどり着くにはアプリを離れる必要があります。アプリ内で直接設定できた方が遥かに便利です。もし変更の必要が滅多にない設定を提供しなければならない時は、[Preferences and Settings Programming Guide](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/UserDefaults/Introduction/Introduction.html)の[Implementing an iOS Settings Bundle](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/UserDefaults/Preferences/Preferences.html)をご覧ください。

[スクショ]

**妥当だと思われる場合は設定アプリへのショートカットを提供しましょう。** アプリ内に「設定 > MyApp > プライバシー > 位置情報サービス」など、ユーザを設定アプリに誘導するテキストが存在している場合は、その場所が自動で開くボタンを用意してあげましょう。開発者向けガイダンスは[UIApplication](https://developer.apple.com/documentation/uikit/uiapplication)の[openSettingsURLString](https://developer.apple.com/documentation/uikit/uiapplication/1623042-opensettingsurlstring)をご覧ください。