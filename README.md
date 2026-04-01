PushToEducation

"https://apis.kahoot.it/media-api/youtube/key" から毎晩最新の key を取得し、"youtubeeducation.com" の埋め込み用パラメータを生成して保存します。

保存されているファイル

keys/
├─ key.json
├─ key1.json
├─ key2.json
├─ key3.json
└─ key4.json

key.json

最新の "enc" 用 key のみを保存しています。

{
  "key": "取得したkey"
}

この "key" は "embed_config" の "enc" に使用します。

例:

?embed_config={"enc":"取得したkey"}

---

key1.json ～ key4.json

"key1.json" ～ "key4.json" には、すぐに使える埋め込みパラメータが "result" として保存されています。

key1.json

タイトル表示あり / 操作バーあり / 全画面あり

controls=1
fs=1
hideTitle=false

key2.json

タイトル非表示 / 操作バーあり / 全画面あり

controls=1
fs=1
hideTitle=true

key3.json

タイトル表示あり / 操作バーなし / 全画面なし

controls=0
fs=0
hideTitle=false

key4.json

タイトル非表示 / 操作バーなし / 全画面なし

controls=0
fs=0
hideTitle=true

---

使い方

動画IDが "dQw4w9WgXcQ" の場合、"key1.json" の "result" を後ろにつけると:

https://www.youtubeeducation.com/embed/dQw4w9WgXcQ?autoplay=1&mute=0&controls=1...

のような再生URLになります。

"result" の中の "&amp;" は HTML用の表記で、実際には "&" と同じです。

例:

?autoplay=1&amp;mute=0

↓

?autoplay=1&mute=0

---

各パラメータの意味

パラメータ| 意味
autoplay=1| 自動再生
mute=0| ミュートしない
controls=1| 再生バーを表示
controls=0| 再生バーを非表示
fs=1| 全画面ボタンを表示
fs=0| 全画面ボタンを非表示
hideTitle=true| 動画タイトルを隠す
hideTitle=false| 動画タイトルを表示
origin| 埋め込み元 ("create.kahoot.it")
forigin| Kahoot の learner ページ
embed_config| "enc" や "hideTitle" を渡す設定

---

協力者 / Contributors

"Toka_Kun_" (https://github.com/toka-kun) | Education Parameter の提供
