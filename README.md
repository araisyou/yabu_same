# VR流鏑馬（やぶさめ）ゲーム（Unity / OpenXR）

VRで流鏑馬（馬上から弓矢を放つ）を体験できるミニゲームです。  
**弓に矢をつがえ、引き、放つ**までをVRコントローラー操作で行い、実際に射っているような操作感を目指しました。

---

## デモの流れ（遊び方）

1. ゲーム開始後、目の前にある**看板**を弓で射ってください  
2. 看板に当たるとイベントが発火し、**ウマが走り出します**

---

## 操作方法（VRコントローラー）

- **矢をつがえる**：左右のハンドコントローラーを重ねる（弓に矢を装填）
- **弓を引く**：右のハンドコントローラーのボタンを押しながら、右手コントローラーを離す（弓を引っ張る）
- **発射**：右のボタンを離す

---

## セットアップ（Unity / OpenXR）

### 1. XR Plug-in Management を有効化

1. `Edit > Project Settings > XR Plug-in Management` をインストール
2. `XR Plug-in Management > OpenXR` にチェックを付ける
3. `XR Plug-in Management > OpenXR` を再度選択し、`Enabled Interaction Profiles` の **「＋」** を押して **HTC Vive Controller Profile** を追加

---

### 2. XR Interaction Toolkit を導入

1. `Window > Package Manager` を開く
2. `Unity Registry > XR Interaction Toolkit` をインストール
3. `Samples > Starter Assets` を **Import**

---

### 3. Project Validation を Fix

1. `XR Plug-in Management > Project Validation` を選択
2. **Fix All** を押す
3. しばらく待つと警告メッセージが消える

---

### 4. XR Rig をシーンへ追加

1. `Hierarchy` に以下Prefabを追加  
   - `Assets/Samples/XR Interaction Toolkit/3.0.3/Starter Assets/Prefabs/XR Origin (XR Rig).prefab`
2. `XR Origin (XR Rig).prefab` の子オブジェクトのうち不要なものはチェックを外して **非アクティブ** にしておく
3. `/MainCamera` のチェックを外す（非アクティブ）

---

## ゲーム開始方法

- ゲームがスタートしたら、目の前にある**看板**を弓で打ってください  
- 命中すると**ウマが走り出します**

---

## こだわりポイント

- **実際に矢を打っているような操作感**を実現しました

---

## 動作環境（必要なら追記）

- Unity：2022.3 LTS（例）
- XR：OpenXR
- XR Interaction Toolkit：3.x
- Interaction Profile：HTC Vive Controller Profile
