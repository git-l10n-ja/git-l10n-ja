# :wave: Git 日本語翻訳チームへようこそ！

#### ※貢献する前に、下記の各項目を必ずお読み下さい。

## 必須補助プログラム・PO Helper

Git の翻訳をより簡単に管理する為に、Git-l10n の皆さんは git-po-helper と言う補助プログラムを作成しました。必ずお使い下さいね。

詳しいインストール方法はこちらをご覧下さい（英語）：
[git-po-helper/README][]

基本の使い方：

- 翻訳ファイルの内容を更新する為に：

  ```shell
  git-po-helper update ja.po
  ```

- コミットログと翻訳ファイルの構文を確認する為に：

  ```shell
  git-po-helper check-po ja.po
  git-po-helper check-commits
  ```

- 詳しい使い方の情報を表示する為に：

  ```shell
  git-po-helper --help
  ```

## Git-l10n 貢献の条約

[Git-l10n][] に従い各貢献者は次の条約を従わなければなりません：

- po/ja.po と po/TEAMS 以外のファイルを編集しないで下さい。

- 各コミットの件名（コミットログ最初の行）は、 l10n: で始まる必要があります。

  ```
  コミットログの例:

  l10n: Update Japanese translations
  ```

- コミットの件名に英文字以外を記入しないで下さい。

- コミットの件名の長さは50文字以内で、他のコミットログ行の長さは72文字以内になる必要があります。

- 多くのコミットをする代わりに、翻訳を一つのコミットにまとめて下さい。

- 各コミットに Signed-off-by: の行を追加する必要があります。この行を Git に自動的に追加されるには、コミットする時は次のコミットオプションを使えます：

  ```shell
  git commit -s
  ```

  ```
  コミットログの例

  l10n: Update Japanese translations

  Signed-off-by: Momotarou <メールアドレス>
  ```

- コミットする前に、翻訳ファイルの構文を次のコマンドで確認して下さい：

  ```shell
  git-po-helper check-po <ja.po>
  ```

## 翻訳作業を始める

1. このリポジトリをフォーク。
2. 自分のフォークを複製（クローン）。
3. Git を使って ja/master ブランチに移動：

  ```shell
  git checkout ja/master
  ```

4. ja/master ブランチで po フォルダに移動。
5. PO ファイル形式を編集できるプログラム、[Poedit][] または [Gtranslator][] を使って ja.po ファイルを翻訳して下さい。

[git-po-helper/README]: https://github.com/git-l10n/git-po-helper#readme
[Git-l10n]: https://github.com/git-l10n/git-po/
[Poedit]: https://poedit.net/
[Gtranslator]: https://wiki.gnome.org/Apps/Gtranslator/
