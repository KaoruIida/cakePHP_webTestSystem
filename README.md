# CakePHP_Web Test System

『テスト問題システム』<br>
CakePHP3.8で作成した、問題/回答の登録〜テスト〜自動採点できるWebアプリケーション。


## 概要

実装のメインはログイン認証とCRUD機能です。<br>

* ログイン/ログアウト機能
* ユーザー情報の登録・編集・削除機能
* 問題/答えの登録・編集・削除機能
* 問題の回答、自動採点機能
* 過去の採点結果の閲覧機能
* ログイン認証の設定
* 問題/回答の登録数が0の場合、一覧に遷移
* ボタン押下で回答枠を追加(Javascript)
* ユーザー情報のバリデーション機能(Javascript)<br>
* 問題/回答のバリデーション機能(Javascript)<br>

bakeコマンドは使用せずMVCを作成。


## 作業環境
 
使用PC: MacBook<br>
VirtualBox・Vagrantを使ってLAMP環境を構築・検証。

* CakePHP： 3.8
* CentOS： 7.4
* Apache： 2.4
* MySQL： 5.6
* PHP： 7.3


## 技術選定

比較的使われている頻度の高い環境を選択。
* Github・ChatWorkのツールを用いてエンジニア に質問・レビューしやすい環境であること。
* 公式ドキュメント、文献、Qiitaやブログ記事など、検索元は容易であること。


## コード作成ルール

レビューにあたり以下のルールを設定しました。

* 変数の統一。※アッパーキャメルは使用しないこと。<br>
キャメルケース…ローカル変数(controller/view)<br>
スネークケース…グローバル変数　<br>
*  必要に応じて、定数化した方がいい部分は定数化する。
* 配列の書き方を統一。<br>
  ○ : $a = [1, 2, 3];<br>
  × : $a = array(1, 2, 3);<br>
* 使いまわしていない変数は変数にせずそのまま使用する。
*  usersテーブルのdelete_flagはmysql側でデフォルト0を設定。


## 開発工程

### phase.1 <基礎機能の構築>
* 環境の構築
* DBの構築
* ログイン/ログアウト機能の実装
* 問題/回答の登録機能
* 問題/回答の編集機能
* 問題/回答の削除機能
* テスト問題自動採点
* 採点結果履歴の閲覧機能

### phase.2 <機能の追加・改修①>

* ログイン認証の設定
* 問題/回答の登録数が0の場合、一覧に遷移
* ボタン押下で回答枠を追加(Javascript)
* 問題/回答のバリデーション機能(Javascript)
* その他リファクタリング

### phase.3 plans<機能の追加・改修②>
* 管理者権限と一般権限の切り分け
* ユーザー情報の登録機能
* ユーザー情報の編集機能
* ユーザー情報の削除機能
* ユーザー情報のバリデーション機能(Javascript)









