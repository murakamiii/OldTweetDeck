# OldTweetDeck
昔のTweetDeckを取り戻しましょう！無料で！  
現在のところ簡単にインストールできる方法はありませんが、このリポジトリをダウンロードし、パッケージ化されていない拡張機能としてChrome/Edge/Opera/Chromiumベースのブラウザー/Firefoxにインストールできます。  
  
また、2015年のTwitterを取り戻したい場合は [OldTwitter](https://github.com/dimdenGD/OldTwitter) 拡張機能もチェックしてみてください。  
  
![スクリーンショット](https://lune.dimden.dev/9713d947d56.png)  
  
## インストール方法
注意: 拡張機能ファイル(Chromiumの場合はZipファイルを展開したもの、Firefoxの場合はZipファイル)をインストール後に削除しないでください。
### Chromium (Chrome, Edge, Opera, Brave など) 
1. [リリースページ](https://github.com/dimdenGD/OldTweetDeck/releases) から `OldTweetDeckChrome.zip` をダウンロードする
2. Zipファイルを展開する
3. 拡張機能ページを開く (`chrome://extensions`)
4. デベロッパーモードを有効にする (拡張機能ページの右上に切り替えスイッチがあります)
5. "パッケージ化されていない拡張機能を読み込む"をクリックする
6. Zipファイルを展開したフォルダを選択する
7. tweetdeck.twitter.com にアクセスして昔のTweetDeckを楽しむ
8. [開発が継続できるように支援する](https://www.patreon.com/dimdendev)

### Firefox
#### Nightly / Developer Edition
1. [リリースページ](https://github.com/dimdenGD/OldTweetDeck/releases) から `OldTweetDeckChrome.zip` をダウンロードする
2. 高度な設定ページを開く (`about:config`)
3. `xpinstall.signatures.required` の設定を false に変更する
4. アドオンページを開く (`about:addons`)
5. アドオンページ右上の歯車アイコン→"ファイルからアドオンをインストール..."をクリックする
6. ダウンロードしたZipファイルを選択する
7. tweetdeck.twitter.com にアクセスして昔のTweetDeckを楽しむ
8. [開発が継続できるように支援する](https://www.patreon.com/dimdendev)

#### Stable
**Stableバージョンでこの拡張機能を使うことは推奨されません**
1. `about:debugging#/runtime/this-firefox`を開く
2. "一時的なアドオンを読み込む..."をクリックしてダウンロードしたZipファイルを選択する
3. **この方法でインストールした場合、Firefoxを閉じた際に拡張機能が削除されます**
  
### Safari
対応していません  
  
## 更新
TweetDeckのファイルが更新された場合は、タブを再読み込みするだけで拡張機能を再インストールすることなく自動的に更新を受け取れます。 (`localStorage.OTDalwaysUseLocalFiles = '1'`の設定をしている場合を除く)  
拡張機能のファイルが更新された場合は、拡張機能を再インストールすることで更新を受け取れます。  
  
## Better TweetDeck
この拡張機能と一緒に使うことが出来るBetter TweetDeckの[fork](https://github.com/dimdenGD/BetterTweetDeck/releases)を作りました。  
この拡張機能のインストール方法と同じ方法でインストールすることができます。  

## よくある質問
#### Manifest version 2 is deprecated, and support will be removed in 2023. という警告が表示されました
その警告は無視してください。  
   
#### ユーザーカラムや検索カラムが読み込まれません
API制限に達しているため読み込めていません。しばらくしてAPI制限が解除されるとまた表示されます。  
このAPI制限を回避したい場合は F12 を押してコンソールタブを開いた後 `localStorage.abuseAPIkeys = '1'` を貼り付けてエンターキーを押してください。  
これによって複数のAPIキーを使うようになり、倍のAPI呼び出しができるようになりますが、自己責任で利用してください。  
この機能を無効にしたい場合は `delete localStorage.abuseAPIkeys` を貼り付けてエンターキーを押してください。  

## 更新履歴
### 3.0.6
このバージョンではリクエストに傍受を追加しました。  
通常のTwitterをリバースエンジニアリングして、通常のTwitterで使用される対応するリクエストを見つけました。  
TweetDeckがシャットダウンAPIを使用しようとすると、リクエストは新しいエンドポイントにリダイレクトされ、結果は古いフォーマットに変換されます。  
  
ユーザーカラムと検索カラムがAPI制限の影響を受けるようになったことにより読み込めない問題を修正しました。  
最終的にはさらに多くのAPIが壊れることが予想されますが、その度に新しい動作するAPIに置き換えていく予定です。  
実行されるリクエストは通常のTwitterのリクエストと同じであるため、安全です。  

**この拡張機能の開発を続けるために[寄付](https://dimden.dev/donate/)をご検討ください**

<details>
<summary>過去の更新履歴</summary>

#### 3.0.5
バージョン更新

#### 3.0.4
API上限を倍に緩和

#### 3.0.3
固定ツイートも表示するように変更 (最近のツイートの場合)

#### 3.0.2
複数アカウントのタイムラインに常にメインアカウントが表示される問題を修正

#### 3.0.1
バージョン更新

#### 3.0.0
リファラーを削除

#### 2.0.5
2.0.4で修正した問題がFirefoxで発生していたのを修正

#### 2.0.4
新TweetDeckが表示される場合がある問題を修正

#### 2.0.3
manifest V2 がFirefoxで動作しない問題を修正

#### 2.0.2
クリックが反応しない問題を修正

#### 2.0.1
新TweetDeckのheadとbodyを削除

#### 2.0.0
manifest V2 で作り直し外部サーバーを必要としないように変更

#### 1.0.2
恐らく動作する

</details>

## ~~透明性に関する免責事項~~
以前はこの拡張機能の利用に外部サーバーが必要でしたが、拡張機能をmanifest v2で作り直したため必要な全てのファイルが拡張機能自体に同梱されています。  
そのため、外部サーバーは現在必要ありません。  

## 日本語翻訳
[@katabame](https://twitter.com/katabame)  
commit [9cf40d6](https://github.com/dimdenGD/OldTweetDeck/commit/9cf40d6f4bab47b4ae905ad7bf3ba3285cb071b1) 時点の内容が翻訳されています
