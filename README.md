# Laravel5.5 LTS公式ドキュメント翻訳リポジトリ

このリポジトリはPHP Webアプリフレームワーク、Laravel5.5LTSの公式英文ドキュメントを日本語へ翻訳しています。

This is a Japanese translation repository for Laravel 5.5 LTS documentations.

翻訳内容は、<https://readouble.com/laravel/5.5/ja>で公開しています。

> 注意：Laravel開発者のTaylor Otwell氏は英語のネイティプスピーカーです。英語しか理解できません。
> 自分の理解できないものには責任が持てないと言う理由から、
> 公式ドキュメントは英語のみです。そのため、日本語翻訳に対して「公式」と付けることは避けてください。
> 「日本語ドキュメント」、「和訳翻訳ドキュメント」など適切にお呼びください。

### 誤訳／タイポなどの報告

* 誤訳やタイポ、未翻訳部分などを報告する場合、以下の内容を含めてください。
    * ページ（章） GitLabのリポジトリやreadouble.comのURL、もしくはページのタイトル（「キュー」、「認証」）など。ページの特定が容易であれば形式はかまいません。（報告に手間がかかるので、行番号を含めたリンクをわざわざ張る必要はありません。）
    * 問題のある和文と正しいと思われる和文（エディターで検索して該当箇所を見つけます。）
* 用語の不統一に関しては、プロジェクト全体を検索しますので、特定のページを指定する必要はありません。それ以外の表記揺れに関しては、該当ページが分かるようにしてください。（表現上の揺れなどは、一度に変更できません。少しづつ、気がついた時点で修正します。）
* 日本語ドキュメントを利用するのは日本人です。そのため、報告やコメントは日本語で記述してください。
* このリポジトリでは5.5LTSの翻訳和文のみ管理しています。readouble.comで公開している他のバージョンの和文に関しては、@HiroKwsにツイートいただくか、hirokws@gmail.comへご連絡ください。なお、メンテナンス期間をフレームワーク本体と合わせているため、readouble.comで公開している日本語翻訳の旧バージョンは更新していません。バージョン5.5リリース時点で、メンテしている和文の対象バージョンは5.5LTSのみとなります。

#### issueで報告する場合

Issueで報告していただくのが、一番簡単です。

** <https://github.com/laravel-ja/ja-docs-5.5/issues>のページで、"New issue"ボタンをクリックし、issueを発行してご報告ください。

#### プルリクエストで報告する場合

* translation-jaディレクトリ下の日本語翻訳Markdownファイルのみを変更してください。それ以外のファイルは変更しないでください。
* 翻訳対象となるバージョンの原文は、original-enディレクトリ下にあります。Laravelのドキュメントリポの最新版ではないことに注意してください。
* ディレクトリ／ファイル構造を変更しないでください。
* 原文と翻訳の文章構造は一致させてください。原文と翻訳は、空行・タイトル行など行ごとの構造を同一に保っています。これにより、翻訳が原文のどの箇所であるかを簡単に見つけることができます。また、原文の変更を翻訳へ反映させる処理を自動化するにも役立てています。
* 原文／翻訳間のファイル構成の一致のチェック、原文／翻訳間の各ファイルの行構成の一致のチェック、用語の不一致のチェックを行うスクリプトが、scripts/pre-commitです。可能であればこれをコミット前に実行し、確認してください。gawk、awk、sed、bashなどを利用しています。
* pre-commitは、プルリクエスト時にCIでも実行されています。エラーになるものはマージしません。

### ディレクトリ構造

| ディレクトリ／ファイル  | 内容                               |
| ----------------------- | ---------------------------------- |
| original-en    | 翻訳対象原文ブランチの内容                  |
| translation-ja | 日本語翻訳Markdownファイル                  |
| scripts        | 用語統一、文章構造確認などの補助スクリプト   |


### 当リポジトリメンテナー

| 名前      | English Name    | Email             | Twitter   |
| --------- | --------------- | ----------------- | --------- |
| 川瀬 裕久 | Hirohisa Kawase | hirokws@gmail.com | @HiroKws  |
| 森 雄一   | Yuichi Mori | mori.yuichi.12.24@gmail.com |           |

当リポジトリのメンテナーは、5.5リリース直前まで募集していました。

上記２名で和文翻訳、リポジトリ管理を行っています。現在、新しく募集はしていません。メンテナーは追加しません。

尚、メンテナーは翻訳と推敲、リポジトリの管理、Issueの対応を行います。メンテナーのロールを外れた時点で、翻訳に対する権利を放棄することに同意することとします。これにより、翻訳文を修正することなしに、MITライセンス文の権利者より、名前を削除することにも同意することとします。

### タグ

| タグ形式               | 内容                                                       |
| ---------------------- | -----------------------------------------------------------|
| published.YYMMDD.HHMM  | readouble.comへ公開したコミット                            |

`published.YYMMDD.HHMM`形式のタグは、readouble.comなどで翻訳文を読む利用者向けのタグです。この形式のタグ間でdiffを確認してもらうことで、原文と翻訳文の変更点を確認できます。一番最初の全文翻訳時点のタグは`init`です。（原文、翻訳文以外の差分も含まれます。）

なお、タグは川瀬が管理しています。（Gitのコミットのタグです。Issueに対するタグは、メンテナーが自由に付けてかまいません。）

### メンテナンス期間

原則、Laravel5.5LTSのメンテ期間である２年間。次のLTS版がリリースされるまで。２０１９年８月頃までの予定です。

メンテ作業が煩雑になったり、メンテ人員が減った場合は、期間途中でもリポジトリを閉じます。予めご了承ください。
