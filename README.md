# 顧客情報をスマートにスタッフ間で共有・管理できる<br>webアプリケーション『Smart-管理』</br>

![header](/readmeFolder/header.png)</br>
# 概要
業種は特に問わず、お店に来店した顧客の情報をスタッフ間で共有・管理することができるアプリケーション。</br>
現場で働いており、**普段PCやスマートフォンに触り慣れていないような人たちでも、スタッフ間で簡単に共有して記録が残せるようなシンプルなサービスをコンセプト**としました。</br>

# 制作背景
個人店などでは顧客管理を手帳で行っていたり、独自にスタッフがそれぞれメモツールを使って
口頭で都度共有していたり、顧客情報の検索にとても時間と手間が掛かっているという課題が見つかりました。</br>
さらに、他の課題では顧客管理するためだけに、月額料金の高い集客媒体と契約していたりなどの声も上がっており、毎月の掛かるコスト的な課題も見つかりました。</br>

**課題まとめ**</br>
・顧客管理のためだけに、月額数万円以上の費用を掛けてしまっている。</br>
・手帳やメモツールでそれぞれで管理していて、スタッフ間で共有するのに手間がかかっている。</br>
・顧客管理のための、入力や保存に時間が掛かってしまっている。</br>

上記の課題を自分の手で解決したいと考え、このサービスの開発を行いました。</br>

※アプリの作成にあたって、より詳しく下記Qiitaの記事に投稿させて頂きましたので、ご覧頂けますと幸いです。</br>

▶︎ [Qiita 記事](https://qiita.com/derasado/items/ed8b22881c8bc1f28c21)</br>



### アプリURL: https://smart-kanri.com
### サンプルユーザー
### メールアドレス:test@example.com
### パスワード:12345678
</br>

# 管理画面基本操作説明

### ●顧客情報の新規作成</br>
※ログイン後(ユーザー登録必須)</br>

①管理画面TOPから顧客情報新規作成</br>
②項目毎に顧客情報を入力して作成</br>
※お客さんに入力してもらう場合はお客様入力専用ページへ</br>
③顧客情報の作成が完了して、詳細ページで入力した内容を確認</br>

![customer_create](/readmeFolder/admin.png)
### お客さんにタブレットなどを渡して直接入力してもらう場合
![input](/readmeFolder/input.gif)


### ●来店履歴の作成</br>
①来店履歴を作成したい顧客のページに飛ぶ</br>
②来店記録追加のボタンを押す</br>
③各項目を入力後に作成するボタンを押す</br>
④顧客毎の詳細ページ(下部)と、来店記録一覧ページで確認</br>

![visit_create](/readmeFolder/visit_create.gif)

### ●顧客&来店履歴の検索</br>
①顧客情報TOPページで検索したい項目を入力して、検索ボタンを押す</br>
②ページ下部で検索値での該当顧客が表示される</br>
③来店履歴での検索を行う場合は、来店記録一覧ページへ移動</br>
④検索したい項目を入力して、検索ボタンを押す</br>
⑤ページ下部で検索値での該当の来店履歴が表示される。</br>

![search](/readmeFolder/search.gif)


# 使用技術

**バックエンド**<br>
PHP 7.4.21 / Laravel 6.20.27

**フロントエンド**<br>
HTML / CSS / javascript / Bootstrap

**インフラ**<br>
mysql 8.0.25</br>
AWS(EC2, S3, RDS, Route 53, ELB, ACM)</br>
Docker 20.10.6 / Docker compose 1.29.1 (開発環境)


**その他の使用技術**<br>
git(gitHub) / Visual Studio Code / SendGrid(メール)</br>
Adobe XD(画面遷移図) / lucidchart(ER図) / Drawio(AWS構成図)</br>
TablePlus(SQLクライアントツール)

# AWS構成図
![画像](/readmeFolder/AWS.png)

# DB設計
### ・ ER図
![画像](/readmeFolder/ERtables.png)
### ・ 各種テーブル

| **テーブル名** | **定義** |
| ---- | ---- |
| users<br>(ユーザー) | スタッフの登録情報 |
| shops<br>(ショップ) | 店舗の登録情報 |
| sectors<br>(セクター) | 店舗の業種 |
| positions<br>(ポジション) | スタッフの役割 |
| customers<br>(カスタマー) | 顧客の情報|
| visit_histories<br>(ビジットヒストリー) | 顧客の来店履歴の情報|
| menus<br>(メニュー) | 店舗のメニュー情報|

# アプリの機能一覧

### メイン機能

-   **顧客情報の新規作成・表示・編集・削除**（CRUD 処理）
-   **お客様が直接入力する専用の顧客新規作成画面**
-   **来店履歴作成・表示・編集・削除**（CRUD 処理）
-   **顧客毎の写真の表示・編集・削除**
-   **顧客情報に紐づく来店履歴の表示**
-   **顧客情報・来店履歴検索**

<br>

### 認証機能

-   ユーザー登録・ログイン・ログアウト
-   メールアドレス認証
-   メールアドレス変更
-   パスワード再設定
-   ユーザープロフィール編集
-   店舗編集

<br>

## 最後に
大変お忙しい中、最後までご覧いただき誠にありがとうございました。<br>
ご興味を持っていただけましたら、下記リンクもご覧頂けると幸いです。<br>

[→  [自己紹介Wantedly](https://www.wantedly.com/id/satoshi_kitagawa_s): 学歴・職務経歴・webエンジニアを目指す経緯などを記載しています！]</br>
[→  [Qiita記事](https://qiita.com/derasado/items/ed8b22881c8bc1f28c21): 今回作成したPFの背景や、苦労した点、アプリ作成に至るまでの学習内容についてまとめた記事です。]</br>
[→  [Twitter](https://twitter.com/derasado): これまで約半年間日々の学習を記録・発信してきました！]</br>
