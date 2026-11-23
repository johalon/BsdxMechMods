# BSX MOD

BSX 向けの非公式 MOD です。
An unofficial mod for BSX. **English follows the Japanese section.**

---

## 日本語

### 概要

BFE の機体「透」を、BSX の自機として使えるようにする MOD です。

* 機体選択画面の晴嵐の位置に、透を配置しています。
* BFE の通常武装 63 種（Lv3 のみ）、フォースクラッシュ（FC）21 種、BFE のデータに残っていた未使用の隠し武装「マーカーミサイル」をすべて移植しています。
* 見た目・エフェクト・効果音は BFE のものです。
* 原作の動きをできるだけ再現したうえで、BSX で遊びやすいように調整しています。

### 注意

> [!WARNING]
> * **導入前に、必ずセーブデータをバックアップしてください。**
> * 今後のアップデートで技を調整していくため、透を使ったリプレイは、アップデート後に正しく再生できなくなります。
> * `Update3.pac` を使う別の MOD とは同時に使えません。

### 導入方法

1. [Releases](../../releases) から最新の `Update3.pac` をダウンロードし、BSX のインストールフォルダ（`BaldrSky.exe` がある場所）に置きます。すでに `Update3.pac` があれば、フォルダの外へ退避してください。
2. アンインストールは、置いた `Update3.pac` を削除するだけです。ゲーム本体のファイルは書き換えません。

### 武装一覧

各武装の威力・最低補正・属性・EX キャンセルのタイミングは [武装一覧](weapon_list_ja.md)（[CSV](weapon_list_ja.csv)）にまとめています。

### 既知の不具合

* 現在わかっている不具合はありません。

### 移植内容

ほとんどの要素は原作をそのまま移植し、一部にだけ原作と異なる調整を入れています。

#### そのまま移植したもの

* **動きと計算式**: BFE と BSX は、物理もダメージ・補正の計算式もまったく違います。値を目合わせで決めず、両作の計算式を調べたうえで、BFE での動き・ダメージを BSX の式に写しています。
* **威力**: BSX の甲と同じ尺度に換算しています（例: 原作のアームジャブ ≒ 甲のジャブ）。BSX の「甲以外の自機は威力 ×1.5」の仕様も考慮済みです。
* **コンボ補正**: 各武装が原作に近い役割（コンボの序盤向き・後半向きなど）になるように、甲の数値を割り当てています。
* **属性**: 原作の炎・雷の武装は、BSX の燃焼・感電になります。

#### 原作と異なる調整

**ダッシュ**

* ブーストダッシュ: BFE には無いため、回避（ドッジ）用のアクションとして新しく追加しました。
* ノーマルダッシュ: BFE のダッシュは速いため、BSX の通常移動として扱える速さにしています。
* サーチダッシュ: 溜めなしですぐ最高速になり、とても速くしています。原作の上位プレイヤーが使っていた高速ダッシュ（バグ技）を再現するためです。

**ダメージ**

* 通常武装: 最低値（コンボ後半の下限）を、技ごとの役割を原作から保ったまま計算し直しています。目安は、イニシャライザ前は原作よりわずかに弱く、イニシャライザを挟んだコンボ全体では原作の約 2 倍です。
* FC: イニシャライザを使ったコンボを控えめにする代わりに、FC が強い機体にしています。
* 連射系（火炎放射器・ガトリング砲など）: 全弾当てたときの強さは保ち、補正がかかりきったコンボ後半でだけ弱くなるようにしています。

**EX キャンセル**

* 多くの技に、EX キャンセルできるタイミングを設定しています。

**早期廃熱**

* 設置技など一部の武装は、当てた相手がのけぞり・ダウン中でも自機の廃熱が始まります。

**装甲**

* 地上で出した近接技の多くと一部の射撃に、最後の攻撃判定までの装甲を付けています。甲より武装が少ないぶん、コンボの選択肢を増やすためです。

**動き・見た目を変えた主な武装**

| 武装 | 調整 |
|---|---|
| ブーストアッパー・ジャンピングニー | 技の後、着地まで落下して終わる |
| ギャラクティックストライク | 空中でも飛び上がる。攻撃ボタンを離すと溜めを終える。飛び上がりの前進と降下が速い |
| クラッシュハンマー | 高いところから出しても、着地してから攻撃する |
| スライディングキック | 空中で出すと、甲と同じ角度で斜め下へ落ちながら蹴る |
| スウィングワイヤー | 慣性が残る。空中で出すと上昇する |
| シールド | ダッシュ中に出すと甲のように滑る |
| サテライトレーザー | 1 本目を敵の真上に落とし、ビームが甲と同じく敵に乗る |
| ガトリングビット・レーザービット | 敵の近くを回り、敵の高さに合わせて動く |
| スタンロッド | 感電中に少しずつダメージが入り、火花が出る |
| フォトンブラスター | 小さい段階の弾が壁で爆発せず、時間で次の段階へ進む |
| マインスイーパ | 撃ち終わりの硬直も武装でキャンセルできる |
| 月華衝・T・K・O・インペリアルファイナル・キャノンブレイカー | 演出（カメラ・暗転・スロー・拘束）を見やすく |
| ギガンテックフィールド | 場を大きくし、敵を押し出しにくく |
| 透の弾全般 | 敵の弾に対する強さを、甲の同じ種類の弾に合わせた（下げたものはなし） |

---

## English

### Overview

This mod adds **Tooru**, the mech from BFE, as a playable mech in BSX.

* On the mech select screen, Tooru is placed in Seiran's position.
* All of Tooru's weapons are ported: BFE's 63 normal weapons (Lv3 only), the 21 Force Crushes (FC), and "Marker Missile", an unused hidden weapon left in the BFE data.
* Visuals, effects and sound effects come from BFE.
* BFE's movement is reproduced as closely as possible, then tuned to play well in BSX.

### Warnings

> [!WARNING]
> * **Back up your save data before installing.**
> * Moves will keep being tuned in future updates, so replays that use Tooru will not play back correctly after an update.
> * It cannot be used together with another mod that also uses `Update3.pac`.

### Installation

1. Download the latest `Update3.pac` from [Releases](../../releases) and put it in your BSX install folder (where `BaldrSky.exe` is). If an `Update3.pac` is already there, move it out of the folder.
2. To uninstall, just delete the `Update3.pac` you added. No game files are modified.

### Weapon list

Power, minimum damage, element and EX cancel timing for every weapon are in the [weapon list](weapon_list_ja.md) (Japanese; [CSV](weapon_list_ja.csv)).

### Known issues

* There are no known issues at the moment.

### What was ported

Almost everything is ported as it is in BFE; only some parts are deliberately tuned differently.

#### Ported as in BFE

* **Movement and formulas**: BFE and BSX differ completely in physics and in their damage and scaling formulas. Instead of eyeballing values, we studied both games' formulas and mapped Tooru's BFE movement and damage onto BSX's.
* **Power**: converted to the same scale as BSX's Kou (e.g. BFE's Arm Jab ≈ Kou's Jab), taking into account BSX's 1.5x power for player mechs other than Kou.
* **Combo scaling**: each weapon is given Kou's values so that it keeps a role close to the one it had in BFE (combo starter, late-combo move, and so on).
* **Elements**: BFE's fire and lightning weapons burn and shock in BSX.

#### Tuned differently from BFE

**Dashes**

* Boost dash: BFE has none, so it was added as a new dodge action.
* Normal dash: BFE's dash is fast, so it was set to a speed that works as BSX's regular movement.
* Search dash: reaches full speed immediately and is very fast, to reproduce the high-speed dash (a bug technique used by top BFE players).

**Damage**

* Normal weapons: the minimum damage (the floor late in a combo) is recalculated while keeping each move's role from BFE. As a guide, damage before the Initializer is slightly below BFE, and a full combo with the Initializer does about 2x BFE.
* FCs: combos with the Initializer are kept modest, and in exchange Tooru's FCs are strong.
* Rapid-fire weapons (Flamethrower, Gatling Gun, etc.): full damage when every shot lands is kept; they only get weaker late in a combo when scaling is maxed out.

**EX cancel**

* Many moves have EX cancel windows.

**Early heat release**

* Some weapons, such as traps, start your heat release even if the target is already staggered or down.

**Armor**

* Most melee moves and a few shots used on the ground have armor until their last attack. Tooru has fewer weapons than Kou, so this gives more options for building combos.

**Main movement and visual changes**

| Weapon | Change |
|---|---|
| Boost Upper, Jumping Knee | After the move, Tooru falls until landing |
| Galactic Strike | Also rises when used in the air. Releasing the attack button ends the charge. Faster forward rise and dive |
| Crash Hammer | Even from high up, attacks only after landing |
| Sliding Kick | In the air, kicks while falling diagonally at the same angle as Kou's |
| Swing Wire | Keeps momentum. Rises when used in the air |
| Shield | Slides like Kou's when used during a dash |
| Satellite Laser | The first beam drops right above the enemy, and beams ride on the enemy like Kou's |
| Gatling Bit, Laser Bit | Circle close to the enemy and follow its height |
| Stun Rod | Deals small damage with sparks while the enemy is shocked |
| Photon Blaster | The small stage no longer explodes on walls; it moves to the next stage over time |
| Mine Sweeper | The recovery after firing can be canceled with a weapon |
| Gekka-sho, T.K.O., Imperial Final, Cannon Breaker | Clearer presentation (camera, darkening, slow motion, hold) |
| Gigantic Field | Bigger field that pushes enemies out less |
| Tooru's shots in general | Strength against enemy shots matches Kou's shots of the same kind (none lowered) |

---

## 免責事項 / Disclaimer

本 MOD は非公式のファンメイド作品であり、原作の開発元および関係各社とは一切関係ありません。BSX・BFE および本 MOD に含まれる原作の画像・効果音などの著作権は、各権利者に帰属します。本 MOD の使用は自己責任でお願いします。使用によって生じたいかなる損害（セーブデータの破損を含む）についても、作者は責任を負いません。権利者からの申し立てがあった場合は、速やかに公開を停止します。

This mod is an unofficial fan-made work and is not affiliated with the original developer or any related company. BSX, BFE, and the original images, sound effects and other assets included in this mod belong to their respective rights holders. Use this mod at your own risk. The author is not responsible for any damage caused by its use, including corrupted save data. If a rights holder objects, distribution will be stopped promptly.
