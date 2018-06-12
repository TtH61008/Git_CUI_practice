WSLでgitを扱うための練習用です。
行ったコード

git config --global user.email "[email adress]"
git config --global user.name "[UserName]"

git init #現在いるディレクトリをローカルリポジトリ化する（適当）
git commit -m "first commit"　#コミット
git remote add origin https://github.com/TtH61008/Git_CUI_practice.git #リモートリポジトリの登録
git push -u origin master #push