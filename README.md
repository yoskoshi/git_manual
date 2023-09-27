## Githubでコード管理するために必要なGit操作マニュアル(コマンド編)
### githubからVSCode(ゲームの場合はUnity)にプロジェクトを持ってくる方法
1. このGithubリポジトリにアクセス権限をリクエストした覚えのない人はDiscordのmemoにGithubのユーザー名を書く。

2. 僕がcollaboratorに追加したらその旨をDiscordのmemoで言うので、それを確認したらGithubで登録したメールアドレスのメールボックスでGithubからのメールを確認して、招待を承認する。

3. 招待を承認したらGithubのプロジェクトに該当するリポジトリにアクセスし、緑色のCodeボタンを押す。

![git_clone1](https://github.com/yoskoshi/Escape_Game/assets/110778997/5971a822-4f90-4d63-bf50-17530a39fd4d)

4. 緑色のコードを押したら、HTTPSを選択してその下のURLの右のボタンを押してURLをコピーする。

![git_clone2](https://github.com/yoskoshi/Escape_Game/assets/110778997/3414ac00-8379-4a5c-8f39-a8c1a333c225)

5. githubのプロジェクトを入れたいディレクトリまで移動して、`git clone コピーしたURL`というコマンドをターミナル(Mac)またはコマンドプロンプト(windows)に打って下の画像のようなのが出るか確認する。

![git_clone3](https://github.com/yoskoshi/Escape_Game/assets/110778997/8b418c5f-a210-41c5-ac06-7c4d0e801ba7)

6. 移動しているディレクトリの中にプロジェクトが入っていると思うので、そのプロジェクトをVSCode(ゲームの場合はUnity)で開く。

### 変更内容をgithubに載せる方法
1. プロジェクトまでディレクトリを移動する。

2. `git checkout -b 作りたい機能のブランチ名`をターミナル(Mac)またはコマンドプロンプト(windows)に打って、VSCodeの左下に画像のように作りたい機能のブランチ名があるか確認。(Unityの場合はブランチ名が表示されないので、`git branch`で作りたい機能のブランチ名に他とは違う色が着いているか確認する)

![git_push1](https://github.com/yoskoshi/Escape_Game/assets/110778997/d2f1dd07-b0e2-457a-a12e-4470ef90eb0f)

3. 機能を実装する。

4. 実装できたら、`git status`で以下の画像のように自分が変更したファイルが赤くなっているか確認する。

![git_push2](https://github.com/yoskoshi/Escape_Game/assets/110778997/5f1612c9-dae1-4964-b6a7-56cbab8858f5)

5. 確認できたら、`git add 変更したファイル名`をターミナル(Mac)またはコマンドプロンプト(windows)に打つ。

6. もう一回`git status`をターミナル(Mac)またはコマンドプロンプト(windows)に打って、以下の画像のように変更したファイルが緑色になっているか確認する。

![git_push3](https://github.com/yoskoshi/Escape_Game/assets/110778997/7fe155a8-7880-4625-85c0-b1c7e37a252f)

7. 確認できたら、`git commit -m "<ここに作った機能の説明をする>"`をターミナル(Mac)またはコマンドプロンプト(windows)に打って、以下の画像のようになったか確認する。

![git_push4](https://github.com/yoskoshi/Escape_Game/assets/110778997/2a74e2ba-9d89-4a9a-b75e-0d9ae782d823)

8. 確認できたら、`git push origin 作ったブランチの名前`をターミナル(Mac)またはコマンドプロンプト(windows)に打って、以下の画像のようになったか確認する。

![git_push5](https://github.com/yoskoshi/Escape_Game/assets/110778997/bbe83d3f-69ef-4a5c-8fc5-6a3ac7a572d3)

### PullRequestを出す方法
1. githubにpushしたら、githubに戻って以下の画像のように緑色のボタンを押す。

![git_pull_request1](https://github.com/yoskoshi/Escape_Game/assets/110778997/4e48266c-06b4-47a3-97fd-4b21d7ad204a)

2. 以下の画像のようにタイトルには作った機能を書き、その下の本文には実装した内容や実際に動作している動画などを載せて、Create Pull Requestボタンを押す。

![git_pull_request2](https://github.com/yoskoshi/Escape_Game/assets/110778997/516db80b-2b0e-42ec-aa47-9abcb2fd7c31)

3. PullRequestが作れたら、Discordの方にPullRequestのURLを添付して送る。

### PullRequestがマージされてからやること
1. 動作確認できたら、マージしてDiscordで知らせるので、マージされた旨が届いたか確認する。

2. 確認したら、`git checkout main`をターミナル(Mac)またはコマンドプロンプト(windows)に打って、mainブランチに戻る。

3. `git fetch`をターミナル(Mac)またはコマンドプロンプト(windows)に打って、以下の画像のようになるか確認する。

![git_pull1](https://github.com/yoskoshi/Escape_Game/assets/110778997/af6f8279-e63c-4bd2-b456-8f9f75527266)

4. `git pull origin main`をターミナル(Mac)またはコマンドプロンプト(windows)に打って、以下の画像のようになるか確認する。
![git_pull2](https://github.com/yoskoshi/Escape_Game/assets/110778997/c12fe2f5-1c81-49a5-879e-931ac624d389)

5. 今作業しているブランチがある場合は`git checkout ブランチ名`をターミナル(Mac)またはコマンドプロンプト(windows)に打つ。

6. `git merge origin/main`をターミナル(Mac)またはコマンドプロンプト(windows)に打って、以下の画像のようになるか確認する。

![git_pull3](https://github.com/yoskoshi/Escape_Game/assets/110778997/574b176a-4543-4a9b-9d36-62ce886c04a8)

7. iキー -> escキー -> 「:wq」を順に行いEnterを押して、以下の画像のようになっているか確認する。ここまでできたら今行っているブランチを最新にすることができ、Githubのエラーが起きることがなくなる。

![git_pull4](https://github.com/yoskoshi/Escape_Game/assets/110778997/d9f63be0-c5a2-4cf7-bb8e-532d98f59b91)

### 注意点
「変更内容をgithubに載せる方法」の3番まで終わったら、「PullRequestがマージされてからやること」の2番から順に行ってほしいです。
理由はいつ誰がgithubを更新するかは不定期なためです。これをしなかったがために面倒くさいエラーに引っ掛かることもあるので、必ずしてください！
`git fetch`で何も出てこなかったら、そのまま作業に戻っていいです！
