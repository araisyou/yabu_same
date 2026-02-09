VR流鏑馬（やぶさめ）ゲーム（Unity / OpenXR）

VRで流鏑馬（馬上から弓矢を放つ）を体験できるミニゲームです。
弓に矢をつがえ、引き、放つまでをVRコントローラー操作で行い、実際に射っているような操作感を目指しました。

デモの流れ（遊び方）

ゲーム開始後、目の前にある看板を弓で射ってください

看板に当たるとイベントが発火し、馬が走り出します

走行中に的を狙って射撃します（スコアや的の種類は必要に応じて追記）

操作方法（VRコントローラー）

矢をつがえる：左右のハンドコントローラーを重ねる（弓に矢を装填）

弓を引く：右手コントローラーのボタンを押しながら、右手を離す（弓を引く動作）

発射：右手のボタンを離す

※ボタンの種類（Trigger / Grip など）を明記したい場合は、実装に合わせて追記してください。

セットアップ（Unity / OpenXR）
1. XR Plug-in Management を有効化

Edit > Project Settings > XR Plug-in Management をインストール

XR Plug-in Management > OpenXR にチェックを付ける

XR Plug-in Management > OpenXR を再度選択し、
Enabled Interaction Profiles の 「＋」 から HTC Vive Controller Profile を追加

2. XR Interaction Toolkit を導入

Window > Package Manager を開く

Unity Registry > XR Interaction Toolkit をインストール

Samples > Starter Assets を Import

3. Project Validation を Fix

XR Plug-in Management > Project Validation を開く

Fix All を押す

しばらく待ち、警告メッセージが消えることを確認

4. XR Rig をシーンへ追加

Hierarchy に以下Prefabを追加

Assets/Samples/XR Interaction Toolkit/3.0.3/Starter Assets/Prefabs/XR Origin (XR Rig).prefab

XR Origin (XR Rig) の子オブジェクトで不要なものはチェックを外して 非アクティブ にする

MainCamera のチェックを外す（非アクティブ）

こだわりポイント

矢をつがえる → 引く → 放つの一連動作をVR操作として成立させ、
**「実際に矢を射っているような操作感」**を重視して設計しました。

動作環境（例）

Unity：（例）2022.3 LTS

XR：OpenXR

Interaction：XR Interaction Toolkit

Controller Profile：HTC Vive Controller Profile

※Unityバージョンや実機（Vive / Index / Quest Linkなど）を確定しているなら、ここを具体化すると強いです。

注意事項 / 既知の問題（必要なら）

（例）初回起動時にOpenXR周りの警告が出る場合は Project Validation > Fix All を再実行してください

（例）コントローラー割り当てが環境で異なる場合があります

ライセンス
