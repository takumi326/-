# サービス名: [タスマネ](https://tasumane.vercel.app/top)

## サービス概要
タスマネはタスク管理とお金管理のサービスです。このサービスはリピート機能を取り入れて管理の手間をできるだけ省いたり、カレンダー機能によって視覚的にわかりやすくしています。またお金管理の機能では現時点で持っている金額からリピート機能を使って毎月の収入と支出の差から自動で翌月以降の月始めにどのくらい残っているかを算出します。


## このサービスへの思い・作りたい理由
高校生のときからお小遣いやお年玉の管理をしていて、来月これ欲しいからこのくらい残すために今月はいくらまで使ってもいいのか、1年後に発売するもののために毎月いくらづつ残していけばいいのかなどをよく計算していました。大学生になってからはPCが手に入ったのでエクセルを用いて同じようなことを見やすく作ったりもしていました。今でもそれは続けていて最低限の給料と支出をいれて1年後にはどれくらい貯金が貯められるのかを確認したりしてます。ただエクセルというのもあって改善を重ねても毎月の固定支出や収入を入力するのが面倒だったり、見やすさを重視しようとするとシートが複数枚になってしまって利便性が落ちるといったこともありそれならこの機会にアプリにしてしまいたいと考えて作りました。

## 機能紹介

### ログイン前
| Top | 
| --- | 
| ![Image from Gyazo](https://i.gyazo.com/875c5f5703ed0340ffbdd53074bac8a7.png) |
| まずはゲストログインで試してみてください。 | 

| サインアップ | ログイン |
| --- |--- |
| ![Image from Gyazo](https://i.gyazo.com/e5a932187ae647381f7c8b2d4dabb4d3.png) | ![Image from Gyazo](https://i.gyazo.com/6c435ca49e13497f459ec83d73af750d.png) |
| メールアドレスとパスワードでアカウント作成できます。 |メールアドレスとパスワードでログインできます。 |



### ログイン後
#### 共通機能
| カレンダー | テーブル |
| --- | --- |
| ![Image from Gyazo](https://i.gyazo.com/bd680580eb7628a80f4d1ca01545ef6f.gif) | ![Image from Gyazo](https://i.gyazo.com/a7569c4ad5a3c0c6def3d264e1e7278a.gif) |
| カレンダーにはそれぞれの設定した日が表示されます。 | 共通でソート、見出しの表示/非表示、削除機能があります。 |

| リピート作成機能 | リピート詳細機能 |
| --- | --- |
| ![Image from Gyazo](https://i.gyazo.com/3f260c5b15cec5939e3ade285a2bfecd.gif) | ![Image from Gyazo](https://i.gyazo.com/c9bc4a5b15b114fdec619110da2b71cb.gif) |
| リピートの種類、始まりの日時と終わりの日時を入力できます。 | リピートされたものがテーブルで表示されています。削除、追加、カレンダーの表示月のみを表示することができます。 |

#### お金管理
| テーブル | 分類 |
| --- | --- |
| ![Image from Gyazo](https://i.gyazo.com/8887699f71e608005790dbbb4ee5de58.gif) | ![Image from Gyazo](https://i.gyazo.com/aa3850cd6fc9e1623f7464e5f0c7f68f.gif) |
| 新規作成したものが折りたたまれています。 | 支出ではクレジットカードなど、収入では会社などを入力します。 |

| カテゴリー | 残高間での送金 |
| --- | --- |
| ![Image from Gyazo](https://i.gyazo.com/2bb1a7784efb45be739bc7fe54e2eb8b.gif) | ![Image from Gyazo](https://i.gyazo.com/8221265f5bf7838ee4500412c81ac688.gif) |
| 事前によく使いそうなものを何個かリストアップしています。 | 貯金用、給料振込用などで分けた残高間での送金を行えます。 |

| 新規作成（支出/収入） | 新規作成（残高） |
| --- | --- |
| ![Image from Gyazo](https://i.gyazo.com/8bb8d91385eeb8cbda48afdeb5843e7a.gif) | ![Image from Gyazo](https://i.gyazo.com/10ead700fe02633cecbe59e755c3e488.gif) |
|  分類、カテゴリ、金額、リピート設定、日時を入力できます。 | 名称（銀行など）、金額を入力できます。 |

#### 目標/タスク管理
| テーブル　機能1 | テーブル　機能2 |  
| --- |--- |  
| ![Image from Gyazo](https://i.gyazo.com/28a43a32abebb201a3d721627a527b6c.gif) | ![Image from Gyazo](https://i.gyazo.com/93d758e8b8c793f3c4f5eacd8e374795.gif) | 
| 未完了/完了/すべてで表示内容を変更ができます。 | 複数選択の削除ができます。 | 

| 新規作成（目標） | 新規作成（タスク） |
| --- | --- |
| ![Image from Gyazo](https://i.gyazo.com/19811ff6493862e34a92e208bbf55651.gif) | ![Image from Gyazo](https://i.gyazo.com/bd370059732d640cc34b64d640c828be.gif) |
| 目標名（資格、ダイエットなど）、達成したい目標（合格、何点、-5kgなど）、期限を入力できます。 | タスク名（参考書Ｐ1～15、カフェで勉強など）、関連する目標、リピート設定、日時を入力できます |

## 使用技術
| カテゴリ | 技術 |
| --- | --- |
| フロントエンド | Next.js、TypeScript |
| バックエンド | Ruby / Rails(APIモード) |
| データベース | PostgreSQL |
| インフラ | vercel/Fly.io |
| 認証 | device_token_auth |
| 開発環境 | Docker/Docker-compose |

## ER図
![ER図](https://i.gyazo.com/3dbe96f3e36a7cb03e47cb81cb56719b.png)
