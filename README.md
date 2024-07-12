# EasyBuildingSystem_Memo

1. Qキーの入力イベント (Pressed)
   - `BP_EBS_PlayerController > Event Graph > Inputs` タブでトリガーされる。
   - `ShowBuildingMenu` 関数を呼び出す。

2. ShowBuildingMenu関数の呼び出し
   - `BP_EBS_PlayerController > Event Graph > Inputs` から呼び出される。
   - 関数内で `ShowBuildingMenu_BPI` インターフェースを呼び出す。

3. ShowBuildingMenu_BPIの呼び出し
   - `BP_EBS_BuildingComponent > ShowBuildingMenu` 関数内で呼び出される。
   - インターフェースが `UI_EBS_HUD` 内の `Event Show Building Menu BPI` をトリガーする。

4. Show Building Menu BPIイベントの処理
   - `UI_EBS_HUD > Event Graph` で処理される。
   - イベントが `Show Building Menu` 関数を呼び出す。

5. Show Building Menu関数の処理
   - `UI_EBS_HUD > Event Graph` で実行される。
   - メニューの可視化、プレイヤーコントローラーの入力制御、マウスカーソルの表示などが行われる。

EBSは何のの略？
 - Easy Building System
 - Event-Based System：イベント駆動型システム。イベントをトリガーとしてアクションを実行するシステム。
 - Entity Building System：ゲームやシミュレーションで使われるエンティティ（オブジェクト）の構築システム。
