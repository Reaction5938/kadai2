<h1>演習課題(フォークとプルモデル)</h1>
<h2>概要</h2>
<P>演習課題の手順に沿ってリポジトリの作成を行った。</P>
<p>kadai2のリポジトリでは、フォークとプルモデルでのモデルを使用し、役割分担を行った。</p>
<h2>役割分担</h2>
<p><strong>🔴A: リード役 (石井 陸登)</strong></p>
<p><strong>🔵B: 開発者 (檀上 蒼也)</strong></p>
<h3>手順</h3>
<h4>1.AがGitHub上にリモートリポジトリを用意し、index.html（"Hello"と記述）をmainブランチにPushする</h4>
<p>ここでは、ターミナルでリモートリポジトリを制作し、GitとGitHubの連携の確認を行った。</p>

```bash
$ mkdir kadai2
$ cd kadai2
$ git init
$ echo "# kadai2" >> README.md
$ echo "Hello" >> index.html
$ git add .
$ git commit -m "new index.html"
$ gh repo create kadai2 --public --source=. --remote=origin --push
```
<p>下の画像がリモートリポジトリを用意したものである。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 151902" src="https://github.com/user-attachments/assets/eb16a50c-7a4b-438b-be30-6e45e7bfa728" />
<h3>フォークのやり方</h3>

```text
1. 🔍Type / to searshを押す。

2. Aのユーザー名を検索する。

3. Aが作成したリモートリポジトリをクリックし、Forkボタンをクリックする。

4. Create a new fork画面で、Owner *(Bのユーザー名) / Repository name *(リモートリポジトリ名はそのまま)でCreate forkをクリックする。

5. AのリモートリポジトリをBのユーザーアカウントにコピーがされる。
```
<p>下の画像がCreate a new fork画面であり、実行する際の詳細な設定を行うことができる。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152033" src="https://github.com/user-attachments/assets/f10f9a36-a739-4dda-bfae-e28330ca69d9" />
<p>下の画像はCreate forkが無事に完了し、Bのアカウントユーザーにkadai2がコピーを行った後である。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152046" src="https://github.com/user-attachments/assets/96cdf2f6-441f-450a-b447-e854b719f7fc" />
<h4>2.Bがリポジトリをcloneし、作業ブランチを作成。index.htmlを編集してPushし、Aへプルリクエストを出す。</h4>
<p>無事にコピーを完了した後にターミナルでリポジトリをcloneし、作業ブランチを作成した所でviコマンドでindex.htmlを編集、addとcommitコマンド使用した後、Aのユーザーに編集したindex.htmlをプルリクエストを出す。</p>
<p>まずはcloneし、ターミナル上でリモートリポジトリをコピーする</p>

```bash
$ git clone git@github.com:Bのユーザー名/kadai2.git
$ cd kadai2
$ git switch -c tejun2
$ vi index.html
```
<p>viコマンド編集前のindex.html</p>

```text
Hello
```
<p>viコマンド編集後のindex.html</p>

```text
Hello
Hello
```
<p>:wqで保存して終了。</p>
<p>編集したindex.htmlをaddとcommitコマンドを使用後、pushコマンドでAのユーザーにプルリクエストを出す。</p>

```bash
$ git add index.html
$ git commit -m "Add index.html"
$ git push origin tejun2
```
<p>この下の画像がターミナルで正常にpushコマンドが処理された状態である。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152459" src="https://github.com/user-attachments/assets/87680fa6-0c10-42a2-9e31-909d11636019" />
<h3>プルリクエストのやり方</h3>

```text
1. Code画面で、Compare & pull requestボタンを押す。

2. Open a pull requestが表示され、Create pull requestを押す。
```
<p>この下の画像がOpen a pull request画面である。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152510" src="https://github.com/user-attachments/assets/b3bd69b4-b2ca-4982-9657-ad1b80dbba74" />
<p>そして下の画像が、プルダウンの承認を待つ状態である</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152526" src="https://github.com/user-attachments/assets/1a44d83f-3fd4-4fb4-b729-2b5266366867" />
<h3>Merge(マージ)のやり方</h3>
<h4>3. AがBのプルリクエストをレビューし、mainブランチにマージする。</h4>

```text
1. リモートリポジトリ内のPull requestsを押す。

2. Bが作成したプルリクエストをクリックする。
```
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152540" src="https://github.com/user-attachments/assets/606ca1db-1e2b-47d8-9dbb-efaf96b6ddc0" />

```text
3. クリック後、No conflicts with base branchにある、Merge pull requestボタンを押す

4. Commit messageが表示され、Confirm mergeボタンを押す。
```
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152612" src="https://github.com/user-attachments/assets/5d300789-95fd-4a09-91ca-5fe6202db4a7" />
<p>下の画像がマージの処理が正常に終了、mainブランチに統合したこある。</p>
<h3>フォークのやり方</h3>

```text
1. 🔍Type / to searshを押す。

2. Aのユーザー名を検索する。

3. Aが作成したリモートリポジトリをクリックし、Forkボタンをクリックする。

4. Create a new fork画面で、Owner *(Bのユーザー名) / Repository name *(リモートリポジトリ名はそのまま)でCreate forkをクリックする。

5. AのリモートリポジトリをBのユーザーアカウントにコピーがされる。
```
<p>下の画像がCreate a new fork画面であり、実行する際の詳細な設定を行うことができる。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152033" src="https://github.com/user-attachments/assets/f10f9a36-a739-4dda-bfae-e28330ca69d9" />
<p>下の画像はCreate forkが無事に完了し、Bのアカウントユーザーにkadai2がコピーを行った後である。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152046" src="https://github.com/user-attachments/assets/96cdf2f6-441f-450a-b447-e854b719f7fc" />
<h4>2.Bがリポジトリをcloneし、作業ブランチを作成。index.htmlを編集してPushし、Aへプルリクエストを出す。</h4>
<p>無事にコピーを完了した後にターミナルでリポジトリをcloneし、作業ブランチを作成した所でviコマンドでindex.htmlを編集、addとcommitコマンド使用した後、Aのユーザーに編集したindex.htmlをプルリクエストを出す。</p>
<p>まずはcloneし、ターミナル上でリモートリポジトリをコピーする</p>

```bash
$ git clone git@github.com:Bのユーザー名/kadai2.git
$ cd kadai2
$ git switch -c tejun2
$ vi index.html
```
<p>viコマンド編集前のindex.html</p>

```text
Hello
```
<p>viコマンド編集後のindex.html</p>

```text
Hello
Hello
```
<p>これはHelloの下にHelloを追加した後、:wqで保存して終了。</p>
<p>編集したindex.htmlをaddとcommitコマンドを使用後、pushコマンドでリモートリポジトリにアップロードする。</p>

```bash
$ git add index.html
$ git commit -m "Add index.html"
$ git push origin tejun2
```
<p>この下の画像がターミナルで正常にpushコマンドが処理された状態である。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152459" src="https://github.com/user-attachments/assets/87680fa6-0c10-42a2-9e31-909d11636019" />
<h3>プルリクエストのやり方</h3>

```text
1. Code画面で、Compare & pull requestボタンを押す。

2. Open a pull requestが表示され、Create pull requestを押す。
```
<p>この下の画像がOpen a pull request画面である。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152510" src="https://github.com/user-attachments/assets/b3bd69b4-b2ca-4982-9657-ad1b80dbba74" />
<p>そして下の画像が、プルダウンの承認を待つ状態である</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152526" src="https://github.com/user-attachments/assets/1a44d83f-3fd4-4fb4-b729-2b5266366867" />
<h3>Merge(マージ)のやり方</h3>
<h4>3. AがBのプルリクエストをレビューし、mainブランチにマージする。</h4>

```text
1. リモートリポジトリ内のPull requestsを押す。

2. Bが作成したプルリクエストをクリックする。
```
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152540" src="https://github.com/user-attachments/assets/606ca1db-1e2b-47d8-9dbb-efaf96b6ddc0" />

```text
3. クリック後、No conflicts with base branchにある、Merge pull requestボタンを押す

4. Commit messageが表示され、Confirm mergeボタンを押す。
```
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152612" src="https://github.com/user-attachments/assets/5d300789-95fd-4a09-91ca-5fe6202db4a7" />
<p>下の画像がマージの処理が正常に終了、mainブランチに統合した状態となる。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152625" src="https://github.com/user-attachments/assets/1dd57dd4-406d-475e-a9ca-96351a46875a" />
<h4>4. Aがローカルのmainブランチを最新化（pull）し、作業ブランチを作成。index.htmlを編集してPRを作成・マージする。</h4>
<p>次にAのユーザーが、ターミナル上で、mainブランチを最新化した後、新しいブランチを作成する。</p>
<p>新しいブランチの中で、viコマンドを使用し、index.htmlを編集していき、Aのユーザー自身でプルリクエストとマージを行う。</p>
<p>まずは、mainブランチの最新化と作業ブランチの作成</p>

```bash
$ git pull origin main
$ git switch -c  tejun4
```
<p>次にviコマンドによるindex.htmlの編集</p>

```bash
$ vi index.html
```
<p>vi編集前のindex.html</p>

```text
Hello
Hello
```
<p>vi編集後のindex.html</p>

```text
Hello!
Hello!
```
<p>ここでは、Helloの末尾に!を追加し、:wqで保存して終了。</p>
<p>次に、addとcommitコマンドを実行した後、pushコマンドでアップロードする。</p>

```bash
$ git add index.html
$ git commit -m "Add index.html"
$ git push origin tejen4
```
<p>下の画像はBの操作と同じくpushの処理が無事に完了した状態である。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 153259" src="https://github.com/user-attachments/assets/48ad752e-ad29-41e0-862c-05183b5c4932" />
<p>次にプルリクエストを作成した後に、マージを行い、mainブランチの統合を行う。</p>

```text
1. Bのユーザーと同じくCode画面でCompare & pull requestボタンを押す。

2. Open a pull requestが表示され、Create pull requestを押す。
```
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 153307" src="https://github.com/user-attachments/assets/c6bded33-257e-4521-a0c9-9d73d413fb77" />

```text
3. クリック後、No conflicts with base branchにある、Merge pull requestボタンを押す
```
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 153319" src="https://github.com/user-attachments/assets/e13ea27e-1f58-4280-a474-5f9a2f32b42f" />

```text
4. 4. Commit messageが表示され、Confirm mergeボタンを押す。
```
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 153326" src="https://github.com/user-attachments/assets/ba1d64b4-976f-4a4b-afff-9cd297bbdc20" />
<p>下の画像が無事にマージまで行い、mainブランチに統合した状態である。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 153335" src="https://github.com/user-attachments/assets/92689ca6-56dd-4eb9-b756-61777e88383e" />
<h4>5. Bがローカルのmainブランチを最新化（pull）し、作業ブランチを作成。stylesheet.cssを追加してAへプルリクエストを出す。</h4>
<p>4.でAが行っていたmainブランチの最新化をBのユーザーが行い、その後に新しい作業ブランチを作成する。</p>

```bash
$ git pull origin main
$ git switch -c tejun5
```
<p>次に、新しい作業ブランチ内でechoコマンドでstylesheet.cssを追加し、addとcommitコマンドで行い、pushコマンドでアップロードしていく。</p>

```bash
$ echo "" >> stylesheet.css
$ git add stylesheet.css
$ git commit -m "Create stylesheet.css"
$ git push origin tejun5
```
<p>その後、アップロードしたstylesheet.cssをプルリクエストをする操作を行う。</p>

```text
1. Code画面で、Compare & pull requestボタンを押す。

2. Open a pull requestが表示され、Create pull requestを押す。
```
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 154203" src="https://github.com/user-attachments/assets/fc30f778-098c-4f28-a675-973d76397458" />
<p>下の画像がプルリクエストを終え、マージの承認待ちの状態である。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 154213" src="https://github.com/user-attachments/assets/ad36f348-969a-412d-8e7c-b69f117f19a6" />
<h4>6. AがBのプルリクエストをレビューし、mainブランチにマージする。</h4>
<p>Bがプルリクエストした内容をAが確認を行い、マージを行う。</p>
<p>下の画像では、Bが作ったプルリクエストが表示されている状態</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 154228" src="https://github.com/user-attachments/assets/5ac5e784-9d5d-4d5f-917d-dbf194fc4ccc" />
<p>次に、プルリクエストをクリックし、Merge pull requestボタンを押す。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 154239" src="https://github.com/user-attachments/assets/ea9a856a-1029-4d5c-ab16-09d0d6cfc35e" />
<p>Merge pull requestボタンを押した後、Commit messageを確認しConfirm mergeボタンを押す。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 154246" src="https://github.com/user-attachments/assets/0ab66f7c-3531-49da-93e3-e812d270675b" />
<p>無事にマージが実行され、下の画像になったら、演習課題の手順である、1～6までの手順を無事に完了したこととなる。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 154257" src="https://github.com/user-attachments/assets/6b8059bb-a116-47aa-a2ee-468ae6692a41" />
