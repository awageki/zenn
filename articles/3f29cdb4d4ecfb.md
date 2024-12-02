---
title: "それなら私はDataGripを使う"
emoji: "🎉"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["DataGrip", "JetBrains", "DB", "AI"]
published: false
---

この記事は、 [PLEX Advent Calendar 2024](https://qiita.com/advent-calendar/2024/plex) の 2 日目の記事です。

## はじめに

同じチームの同僚が、PLEX Advent Calendar 2024 の 1 日目に「[【DB クライアントツール論争】それでも私は DBeaver を使う](https://product.plex.co.jp/entry/dbeaver)」という記事を書いてくれました！
記事では DBeaver という DB クライアントツールが紹介されており、私も布教されましたが（詳しくは記事を見てみてください）元々使っている DataGrip を使い続けています。
そこで、今回の記事では DataGrip という DB クライアントツールについて、簡単に紹介した上でおすすめの機能を紹介していきたいと思います。

## DataGrip とは

JetBrains 社が提供している DB クライアントツールです。
https://www.jetbrains.com/ja-jp/datagrip/

JetBrains 社は [IntelliJ IDEA](https://www.jetbrains.com/ja-jp/idea/) をはじめとした様々な言語の統合開発環境 (IDE) を提供しており、その中のひとつが DataGrip です。
DataGrip は PostgreSQL や MySQL、Oracle をはじめとした複数のデータベースに対応しているほか、最近では AI アシスタントが導入されるなど開発に必要なあらゆる機能が搭載されています。
有料ではありますが、それに見合った機能が提供されており値段相応の価値はあると感じています。

次に普段 DataGrip を使う中で、よく使うショートカットやおすすめの機能を紹介していきます。

## ショートカット

業務で RubyMine を使っていることもあり、ショートカットが JetBrains 社の他の IDE と同じなところもメリットの一つだと感じでいます。
そのうちのいくつかを紹介します。

### 検索まわり

DataGrip の GUI 上で Shift を 2 回クリックする（`Shift` + `Shift`）と Search Everywhere という検索が使えます。
名前の通り、なんでも検索できるので便利です。

https://www.jetbrains.com/help/datagrip/search-in-ide.html#search_everywhere

私がよく使うのは、その中でも Database 検索（`Сmd` + `O`）でテーブル名を入力することで、見たいテーブルをすぐに表示することができます。

![テーブルの検索](https://storage.googleapis.com/zenn-user-upload/6c07f1ddb386-20241202.gif)

### クエリコンソールまわり

DataGrip では console_1、console_2 のように複数のコンソールを別タブで開いておくことができます。
新しいクエリコンソールを開くショートカットは、`Сmd` + `Shift` + `L` です。
クエリコンソール上で書いたクエリは `Сmd`+`Enter` で実行できます。

また、`Сmd` + `Option` + `E` でこれまで実行した クエリ の履歴が確認できます。
Paste ボタンを押すとクエリがクエリコンソール上に貼り付けされます。
![実行履歴](https://storage.googleapis.com/zenn-user-upload/3cd81083b6c1-20241202.png)

### タブまわり

`Сmd` + `Shift` + `W` で今見ているタブ以外のタブを全て閉じれます。

他にも便利なショートカットが設定されているので、興味がある方は下記のドキュメントに掲載されている、[default keymap reference card (74 KB)](https://resources.jetbrains.com/storage/products/datagrip/docs/DataGrip_keymap.pdf?_gl=1*ko5jbk*_gcl_au*MTgyOTcyNDQ0NC4xNzMxNDg0NjQy*FPAU*MTgyOTcyNDQ0NC4xNzMxNDg0NjQy*_ga*MTYxMDA1MTMxNC4xNzI5NjQ5MjQ5*_ga_9J976DJZ68*MTczMzExMDMxOC44LjEuMTczMzExMDYwNy4xNi4wLjA.) を見てみてください！
https://www.jetbrains.com/help/datagrip/mastering-keyboard-shortcuts.html

## ビジュアライズ

## ER 図

Diagrams を使うと下記のような ER 図を表示してくれます。

https://www.jetbrains.com/help/datagrip/creating-diagrams.html#db_diagrams

![Diagrams](https://storage.googleapis.com/zenn-user-upload/51a1f2c64c98-20241202.png)

![ER図](https://storage.googleapis.com/zenn-user-upload/7123c35827c4-20241202.png)

## 実行計画

クエリコンソール上で実行計画を出した後に、Explain した結果を Diagrams で表示してくれます。

![実行計画](https://storage.googleapis.com/zenn-user-upload/428355d27bd1-20241202.png)

![ビジュアライズ](https://storage.googleapis.com/zenn-user-upload/62660e229132-20241202.png)

https://www.jetbrains.com/help/datagrip/query-execution-plan.html

## そのほか

### pg_dump、pg_restore

データのバックアップを取っておいたり、それをもとにリストアするのも DataGrip なら GUI 上で簡単にできます。

また、pg_dump は下記のようにオプションを指定することで、特定のテーブルのみ対象とすることもできます。
![pg_dump](https://storage.googleapis.com/zenn-user-upload/eafca22bef71-20241202.png)

pg_restore
![pg_restore](https://storage.googleapis.com/zenn-user-upload/0da56a7fcb5e-20241202.png)

## おまけ：AI アシスタント

業務では使用していないですが、トライアルで AI アシスタントを使ってみました。
触ってみて体験が良かった機能についていくつか紹介します。
https://www.jetbrains.com/help/datagrip/ai-assistant.htm

### 導入方法

DataGrip を使っている方はプラグインをインストールするだけで、7 日間トライアルが使えますので（2024 年 12 月 2 日時点）試してみてください。
https://www.jetbrains.com/help/datagrip/ai-assistant.html#activate-ai-assistant-license

### データの取得範囲

AI アシスタントを使うにあたって、データの使用範囲が気になったので調べてみました。
[公式ドキュメント](https://www.jetbrains.com/help/datagrip/ai-assistant.html#how-we-handle-your-code-and-data)では下記のように書かれています。

> When you use AI features, DataGrip needs to send your requests and pieces of your code to the LLM (Large Language Model) provider. Besides the prompts you type, it may send additional details, such as file types, frameworks used, and any other information that may be necessary for providing context to the LLM.

AI 機能を使用する場合、DataGrip はあなたのリクエストとコードの一部を LLM（大規模言語モデル）プロバイダに送信する必要があります。入力したプロンプトの他に、ファイルタイプ、使用したフレームワーク、LLM にコンテキストを提供するために必要なその他の情報などの詳細を送信することがあります。

> In addition, DataGrip builds with the AI Assistant plugin perform opt-in collection of detailed data about the usage of AI features, including the full communication between you and the LLM (both text and code fragments). This data is kept strictly confidential and is used by JetBrains for product improvement purposes only. It is never shared with any external parties, and it will not be used for training any ML models that generate code or text, or revealed in any form to any other users. The option that controls detailed data collection can be found in the IDE Settings under Tools | AI Assistant | Data Sharing | Allow detailed data collection and is disabled by default.

さらに、DataGrip は AI アシスタントプラグインを使用して、あなたと LLM 間の完全な通信（テキストとコードフラグメントの両方）を含む、AI 機能の使用に関する詳細なデータをオプトインで収集します。このデータは厳重に管理され、JetBrains によって製品改良の目的でのみ使用されます。また、コードやテキストを生成する ML モデルのトレーニングに使用されたり、他のユーザーに公開されたりすることはありません。詳細なデータ収集を制御するオプションは、IDE 設定の「ツール｜ AI アシスタント｜データ共有｜詳細なデータ収集を許可」にあり、デフォルトでは無効になっています。

> AI Assistant doesn't share or get access to the data in your database.

AI アシスタントがデータベースのデータを共有したり、アクセスしたりすることはありません。

内容を見ると、「ML モデルのトレーニングに使用されたり、他のユーザーに公開されたりすることはありません」とありますが、業務で使用する際は会社やチームの方針に従った方が良さそうです。
なお、JetBrains 社に情報を共有するかどうかは設定で変更できます。

![設定](https://storage.googleapis.com/zenn-user-upload/3b922312e678-20241202.png)

### 日本語化する

設定の Tools->AI Assistant->Natural Language から AI アシスタントで使用する言語を指定できるので、日本語に設定しておきます。
これでチャットを使う際に日本語で返してくれるようになります。

![](https://storage.googleapis.com/zenn-user-upload/7cb5500fe6fe-20241202.png)

### チャット

2024 年 12 月 2 日時点で使えるモデルは、

- openai-gpt-4o
- openai-gpt-4
- google-chat-gemini-pro-1.5
- google-chat-gemini-flash-1.5
- openai-chat-gpt

でした。
今回の記事では openai-gpt-4o を使って検証を行いました。

実行前にスキーマを正しくアタッチしておくと、テーブル名を明示しなくても正しい SQL を作成してくれました。
簡単なものだったとはいえすごい 😳
![チャット](https://storage.googleapis.com/zenn-user-upload/6283dfd37f80-20241202.gif)

チャット上で作成されたクエリは、ボタンひとつでコンソール上にコピペできます！
![コピペ](https://storage.googleapis.com/zenn-user-upload/5fe675b35554-20241202.gif)

また、実行計画も結果を貼って一言添えるだけで内容を説明してくれます。

![](https://storage.googleapis.com/zenn-user-upload/5107b0c43dac-20241202.png)

### クエリコンソール

クエリコンソール上でも AI アシスタントが使えます。

クエリを選択して右クリックして AI Actions -> Explain Code をすると、そのクエリの内容について説明してくれます。
![](https://storage.googleapis.com/zenn-user-upload/74c49d62d009-20241202.png)

![](https://storage.googleapis.com/zenn-user-upload/507aade2eb65-20241202.png)

同様に AI Actions -> Suggest Refactoring で、そのクエリのリファクタリング案を提示してくてます。

![](https://storage.googleapis.com/zenn-user-upload/313b7876d44f-20241202.png)

![](https://storage.googleapis.com/zenn-user-upload/4a365f9476f2-20241202.png)

他にもクエリ実行時にエラーが出た場合、エラーの内容を説明してくれるほか、修正も行ってくれます。

![](https://storage.googleapis.com/zenn-user-upload/c1c4f21ca1a9-20241202.png)

![](https://storage.googleapis.com/zenn-user-upload/7da9fef3ae0c-20241202.png)

## さいごに

今回の記事では DataGrip について、機能の紹介をメインに行いました。
DataGrip にはデフォルトでリッチな機能が実装されており、使いこなすことで日々の業務効率が大幅に改善すると思います。
AI アシスタントなどまだ十分に試せていない機能もあるため、今後も
