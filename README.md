<h1>演習課題(フォークとプルモデル)</h1>
<h2>概要</h2>
<P>演習課題の手順に沿ってリポジトリの作成を行った。</P>
<p>kadai2のリポジトリでは、フォークとプルモデルでのモデルを使用し、役割分担を行った。</p>
<h2>役割分担</h2>
<p><strong>🔴A：リード役（石井 陸登)</strong></p>
<p><strong>🔵B: 開発者(檀上 蒼也)</strong></p>
<h3>手順</h3>
<h4>1.AがGitHub上にリモートリポジトリを用意し、index.html（"Hello"と記述）をmainブランチにPushする</h4>
<p>ここでは、ターミナルでリモートリポジトリを制作し、GitとGitHubの連携の確認を行った。</p>

```bash
$ mkdir kadai2
$ cd kadai2
$ git init
$ echo "# kadai2" >> README.md
$ git add .
$ git commit -m "new index.html"
$ gh repo create kadai2 --pubilc --source=. --remote=origin --push
```
<p>下の画像がリモートリポジトリを用意したものである。</p>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 151902" src="https://github.com/user-attachments/assets/eb16a50c-7a4b-438b-be30-6e45e7bfa728" />
<h3>フォークとプルモデル</h3>

```text

```
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152033" src="https://github.com/user-attachments/assets/f10f9a36-a739-4dda-bfae-e28330ca69d9" />
<h4>2.Bがリポジトリをcloneし、作業ブランチを作成。index.htmlを編集してPushし、Aへプルリクエストを出す。</h4>
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152540" src="https://github.com/user-attachments/assets/606ca1db-1e2b-47d8-9dbb-efaf96b6ddc0" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152612" src="https://github.com/user-attachments/assets/5d300789-95fd-4a09-91ca-5fe6202db4a7" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152625" src="https://github.com/user-attachments/assets/05e64303-729e-4227-8c88-fd6dfdb643de" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 153259" src="https://github.com/user-attachments/assets/48ad752e-ad29-41e0-862c-05183b5c4932" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 153307" src="https://github.com/user-attachments/assets/c6bded33-257e-4521-a0c9-9d73d413fb77" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 153319" src="https://github.com/user-attachments/assets/e13ea27e-1f58-4280-a474-5f9a2f32b42f" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 153326" src="https://github.com/user-attachments/assets/ba1d64b4-976f-4a4b-afff-9cd297bbdc20" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 153335" src="https://github.com/user-attachments/assets/92689ca6-56dd-4eb9-b756-61777e88383e" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 154228" src="https://github.com/user-attachments/assets/5ac5e784-9d5d-4d5f-917d-dbf194fc4ccc" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 154239" src="https://github.com/user-attachments/assets/ea9a856a-1029-4d5c-ab16-09d0d6cfc35e" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 154246" src="https://github.com/user-attachments/assets/0ab66f7c-3531-49da-93e3-e812d270675b" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 154257" src="https://github.com/user-attachments/assets/6b8059bb-a116-47aa-a2ee-468ae6692a41" />

<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152046" src="https://github.com/user-attachments/assets/96cdf2f6-441f-450a-b447-e854b719f7fc" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152459" src="https://github.com/user-attachments/assets/87680fa6-0c10-42a2-9e31-909d11636019" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152510" src="https://github.com/user-attachments/assets/b3bd69b4-b2ca-4982-9657-ad1b80dbba74" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 152526" src="https://github.com/user-attachments/assets/1a44d83f-3fd4-4fb4-b729-2b5266366867" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 154203" src="https://github.com/user-attachments/assets/fc30f778-098c-4f28-a675-973d76397458" />
<img width="1920" height="1032" alt="スクリーンショット 2026-08-24 154213" src="https://github.com/user-attachments/assets/ad36f348-969a-412d-8e7c-b69f117f19a6" />
