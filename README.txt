WSLでgitを扱うための練習用です。
経験したコード

▶ gitの初期設定。たぶん最初の一回だけでいい。
git config --global user.email "[email adress]"
git config --global user.name "[UserName]"

▶ 基本操作
git init #現在いるディレクトリをローカルリポジトリ化する（適当）
git add --all #編集したファイルをすべてステージングする。望ましくはない。
git commit -m "[コミットへのコメント]"　#コミット
git remote add origin https://github.com/TtH61008/Git_CUI_practice.git #リモートリポジトリの登録
git push -u origin master #push

▶ ローカルブランチ操作
git status #現在の状態を見る
git branch #ローカルのブランチを見る
git branch -a #リモートも含めたリポジトリを見る。WSLだと赤字がリモート。
git branch [ブランチ名] #ローカルブランチの作成
git checkout [ブランチ名] #ローカルブランチへの移動
git checkout -b [ブランチ名] #ローカルブランチの作成と移動を同時に行う。
git branch delete [ブランチ名] #ローカルブランチ削除

▶ リモートブランチ操作（主にpush）
git push #現在のブランチがリモートブランチと結びついていれば、pushする。
git push -u origin [ローカルブランチ名] #ローカルブランチをリモートにpushする。-uでリモートとの結びつけを同時に行う。同名のリモートブランチが無ければ作成する？
git push -u origin [ローカルブランチ名]:[リモートブランチ名] #リモートブランチに違う名前を付けたい時に利用
git push origin :[リモートブランチ名] #リモートブランチ削除

▶ 応用編
git add -p [ファイル名] #ファイル名の一部だけaddすることができる……のだが、いまいち使い方がわからない。その後の対話にeを入力することで一行ごと編集できるが、patchがエラーになる……

