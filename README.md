# BSX MOD

BSX 向けの非公式 MOD です。
An unofficial mod for BSX. **English follows the Japanese section.**

---

## 日本語

### 概要

BFE の機体「透」を、BSX の自機として使えるようにする MOD です。

* 機体選択画面の晴嵐の位置に、透を配置しています。
* 武装は BFE の通常武装 63 種（Lv3 のみ）、必殺技（FC）21 種、BFE のデータに残っていた未使用の隠し武装「マーカーミサイル」をすべて移植しています。
* 見た目・エフェクト・効果音は BFE のものです。
* 原作の動きをできるだけ再現したうえで、BSX で遊びやすいように調整した「改善版」です。

### 注意

> [!WARNING]
> * **導入前に、必ずセーブデータをバックアップしてください。**
> * 今後のアップデートで透の技を調整していくため、透を使ったリプレイは、アップデート後に正しく再生できなくなります。
> * `Update3.pac` を使う別の MOD とは同時に使えません。

### 導入方法

1. [Releases](../../releases) から最新の `Update3.pac` をダウンロードし、BSX のインストールフォルダ（`BaldrSky.exe` がある場所）に置きます。
2. すでに `Update3.pac` がある場合（別の MOD など）は、フォルダの外へ退避してから置いてください。

アンインストールは、置いた `Update3.pac` を削除するだけです。ゲーム本体のファイルは書き換えません。

### 武装一覧

各武装の威力・最低補正・属性・EX キャンセルできるタイミングは [武装一覧（weapon_list_ja.md）](weapon_list_ja.md) にまとめています（CSV 版: [weapon_list_ja.csv](weapon_list_ja.csv)）。

### 既知の不具合

* 現在わかっている不具合はありません。
* 不具合を見つけたら、[Issues](../../issues) で教えてください（どの武装で、地上・空中のどちらで出したか、可能なら動画）。

### 移植内容

ほとんどの要素は原作をそのまま移植し、一部にだけ原作と異なる調整を入れています。

#### そのまま移植したもの

* **動きと計算式**: BFE と BSX では、物理も、ダメージと補正の計算式もまったく違います。値を目合わせで決めるのではなく、両作の計算式を調べたうえで、BFE での動き・ダメージを BSX の式に写しています。
* **威力**: BSX の甲と同じ尺度になるように換算しています（例: 原作のアームジャブ ≒ 甲のジャブ）。BSX の「甲以外の自機は威力 ×1.5」の仕様も考慮したうえでの強さです。
* **コンボ補正**: 各武装が原作に近い役割（コンボの序盤向き・後半向きなど）になるように、甲の数値を割り当てています。
* **属性**: 原作の炎・雷の武装は、BSX の燃焼・感電になります。

#### 原作と異なる調整

**ダッシュ**

* ブーストダッシュ: BFE には無いため、移動用ではなく回避（ドッジ）用の新規アクションとして追加しました。
* ノーマルダッシュ（通常移動）: BFE のダッシュは速いため、BSX の通常移動として扱える速さにしています。
* サーチダッシュ: BFE のダッシュには溜めが無いため、溜めなしですぐ最高速になる形にしています。

**ダメージ**

* 通常武装: 最低値（コンボ後半でダメージが下がりきったときの下限）を、技ごとの役割を原作から保ったまま計算し直しています。目安は、イニシャライザを使う前は原作よりわずかに弱く、イニシャライザを挟んだコンボ全体では原作の約 2 倍です。
* FC（必殺技）: イニシャライザを使ったコンボを控えめにする代わりに、FC が強い機体にしています。FC は補正なしで全段当てたときの合計が 1000 前後になるように威力を上げ、最低値は原則として表示威力の 60% にしています（T・K・O・キャノンブレイカー・エクスカリバーは 100%、インペリアルファイナル・集束波動砲・ジェノサイド・ショットガンは 80%）。
* 連射系（火炎放射器・ガトリング砲など）: 素で全弾当てたときの強さは保ち、補正がかかりきったコンボ後半でだけ弱くなるようにしています。
* 個別の値は [武装一覧](weapon_list_ja.md) を見てください。

**EX キャンセル**

* 41 の技に、EX キャンセルできるタイミングを設定しています。タイミングは武装一覧に載せています。

**早期廃熱**

* 設置技・弾が後から当たる技など一部の武装は、当てた相手がのけぞり・ダウン中でも自機の廃熱が始まります（武装一覧の「早期廃熱」欄）。

**装甲**

* 地上で出した近接技の多くと一部の射撃に、出してから最後の攻撃判定までの装甲を付けています。

**動き・見た目を変えた主な武装**

| 武装 | 調整 |
|---|---|
| ブーストアッパー・ジャンピングニー | 技の後、着地まで落下して終わる |
| ギャラクティックストライク | 空中でも飛び上がる。攻撃ボタンを離すと溜めを終える。飛び上がりの前進と降下を速く |
| クラッシュハンマー | 高いところから出しても、着地するまで落ちてから攻撃する |
| スライディングキック | 空中で出すと、甲と同じ角度で斜め下へ落ちながら蹴る |
| スウィングワイヤー | 慣性が残り、空中で使える動きにした（甲を参考） |
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
* All of Tooru's weapons are ported: the 63 normal weapons of BFE (Lv3 only), the 21 Force Crushes (FC), and "Marker Missile", an unused hidden weapon left in the BFE data.
* Visuals, effects and sound effects come from BFE.
* This is the "improved" version: it reproduces BFE's movement as closely as possible, then tunes it to play well in BSX.

### Warnings

> [!WARNING]
> * **Back up your save data before installing.**
> * Tooru's moves will keep being tuned in future updates, so replays that use Tooru will not play back correctly after an update.
> * It cannot be used together with another mod that also uses `Update3.pac`.

### Installation

1. Download the latest `Update3.pac` from [Releases](../../releases) and put it in your BSX install folder (where `BaldrSky.exe` is).
2. If an `Update3.pac` is already there (from another mod, for example), move it out of the folder first.

To uninstall, just delete the `Update3.pac` you added. No game files are modified.

### Weapon list

Power, minimum damage, element and EX cancel timing for every weapon are listed in [weapon_list_ja.md](weapon_list_ja.md) (Japanese; CSV: [weapon_list_ja.csv](weapon_list_ja.csv)).

### Known issues

* There are no known issues at the moment.
* If you find a bug, please report it in [Issues](../../issues) (which weapon, whether used on the ground or in the air, and a video if possible).

### What was ported

Almost everything is ported as it is in BFE; only some parts are deliberately tuned differently.

#### Ported as in BFE

* **Movement and formulas**: BFE and BSX differ completely in physics and in their damage and combo-scaling formulas. Instead of eyeballing values, we studied both games' formulas and mapped Tooru's BFE movement and damage onto BSX's.
* **Power**: converted to the same scale as BSX's Kou (e.g. BFE's Arm Jab ≈ Kou's Jab). The strength accounts for BSX's rule that player mechs other than Kou get 1.5x power.
* **Combo scaling**: each weapon is given Kou's values so that it plays a role close to the one it had in BFE (good as a combo starter, good late in a combo, and so on).
* **Elements**: BFE's fire and lightning weapons burn and shock in BSX.

#### Tuned differently from BFE

**Dashes**

* Boost dash: BFE has none, so it was added as a new action, a dodge rather than a way to travel.
* Normal dash (regular movement): BFE's dash is fast, so it was set to a speed that works as BSX's regular movement.
* Search dash: BFE's dash has no wind-up, so the search dash reaches full speed immediately.

**Damage**

* Normal weapons: the minimum damage (the floor reached late in a combo) is recalculated while keeping each move's role from BFE. As a guide, before using the Initializer the damage is slightly below BFE, and a full combo with the Initializer does about 2x BFE.
* FCs: combos with the Initializer are kept modest, and in exchange Tooru's FCs are strong. FC power is raised so that landing every hit with no scaling totals around 1000, and the minimum damage is generally 60% of the displayed power (100% for T.K.O., Cannon Breaker and Excalibur; 80% for Imperial Final, Focused Wave Cannon and Genocide Shotgun).
* Rapid-fire weapons (Flamethrower, Gatling Gun, etc.): full damage when every shot lands is kept; they only get weaker late in a combo when scaling is maxed out.
* See the [weapon list](weapon_list_ja.md) for individual values.

**EX cancel**

* 41 moves have EX cancel windows. The windows are in the weapon list.

**Early heat release**

* Some weapons, such as traps and moves whose shots hit later, start your heat release even if the target is already staggered or down (the 早期廃熱 column of the weapon list).

**Armor**

* Most melee moves and a few shots used on the ground have armor from startup until their last attack.

**Main movement and visual changes**

| Weapon | Change |
|---|---|
| Boost Upper, Jumping Knee | After the move, Tooru falls until landing |
| Galactic Strike | Also rises when used in the air. Releasing the attack button ends the charge. Faster forward rise and dive |
| Crash Hammer | Even from high up, falls until landing before attacking |
| Sliding Kick | In the air, kicks while falling diagonally at the same angle as Kou's |
| Swing Wire | Keeps momentum and is usable in the air (modeled on Kou) |
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
