---
title: "【フェデレーテッドユーザーの方へ】CodeCommitをCLIとVSCodeに接続しよう"
emoji: "⛳"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: [AWS,Git]
published: false
---
## はじめに
最近業務で GitLub →　CodeCommit に移行したのですが、VSCodeにフェデレーテッドユーザーの認証情報を登録する時に詰まってしまいました。

自身のアカウントだと出来るんだけど、接続時に必要になるユーザー名とパスワードどうやるんだろーって方、いますよね。(私です)

ということで、一緒に認証方法について見ていきましょう。

## CodeCommitの認証方法について
まずは認証方法についてみていきましょう。

下記の公式ドキュメントを...
見て理解できる方は理解できると思いますが、私はぱっと見理解できませんでした...!

https://docs.aws.amazon.com/ja_jp/codecommit/latest/userguide/auth-and-access-control.html

https://docs.aws.amazon.com/ja_jp/IAM/latest/UserGuide/id_credentials_ssh-keys.html

https://docs.aws.amazon.com/ja_jp/codecommit/latest/userguide/setting-up-git-remote-codecommit.html

https://docs.aws.amazon.com/ja_jp/codecommit/latest/userguide/setting-up-https-windows.html

https://docs.aws.amazon.com/ja_jp/codecommit/latest/userguide/setting-up-https-unixes.html

ということで簡単にまとめると、CodeCommitへの認証方法は4つくらいあるようです。
- HTTPS
- SSH
- git-remote-codecommit
- AWS CLI の credential-helper
