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

### 注意

> [!WARNING]
> * **導入前に、必ずセーブデータをバックアップしてください。**
> * 今後のアップデートで透の技を調整していくため、透を使ったリプレイは、アップデート後に正しく再生できなくなります。

### 導入方法

1. [Releases](../../releases) から最新の `Update3.pac` をダウンロードし、BSX のインストールフォルダ（`BaldrSky.exe` がある場所）に置きます。
2. ほかの MOD など、競合しそうなファイルがあれば、フォルダの外へ退避してください。

アンインストールは、置いた `Update3.pac` を削除するだけです。

### 既知の不具合

* メガ・ブーストアッパーのヒット数が原作と違う。
* スタンロッドの効果音が重なって聞こえる。
* 鷹落としに複数の不具合がある。

### 移植内容

ほとんどの要素は原作をそのまま移植し、一部にだけ原作と異なる調整を入れています。

#### そのまま移植したもの

* **動きと計算式**: BFE と BSX では、物理も、ダメージと補正の計算式もまったく違います。値を目合わせで決めるのではなく、両作の計算式を調べたうえで、BFE での動き・ダメージを BSX の式に写しています。
* **威力**: BSX の甲と同じ尺度になるように換算しています（例: 原作のアームジャブ ≒ 甲のジャブ）。BSX の「甲以外の自機は威力 ×1.5」の仕様も考慮したうえでの強さです。
* **コンボ補正**: 各武装が原作に近い役割（コンボの序盤向き・後半向きなど）になるように、甲の数値を割り当てています。

#### 原作と異なる調整

**ダッシュ**

* ブーストダッシュ: BFE には無いため、移動用ではなく回避（ドッジ）用の新規アクションとして追加しました。
* ノーマルダッシュ（通常移動）: BFE のダッシュは速いため、BSX の通常移動として扱える速さにしています。
* サーチダッシュ: BFE のダッシュには溜めが無いため、溜めなしですぐ最高速になる形にしています。

**ダメージ（全体）**

* 最低値（コンボ後半でダメージが下がりきったときの下限）を、技ごとの役割を原作から保ったまま計算し直しています。目安は、イニシャライザを使う前は原作よりわずかに弱く、イニシャライザを挟んだコンボ全体では原作の約 2 倍です。
* FC（必殺技）は、すべて最低値を表示威力の 80% 以上にしています。BSX ではイニシャライザ後の FC で補正が 50% にリセットされるため、そこから救ってカタルシスを得られるようにするためです。

**個別に調整した武装**

| 武装 | 調整 | 意図 |
|---|---|---|
| ドリル | 最低値を表示威力の 100% 以上 | 武装説明の「補正に強い」どおり、コンボ後半でも頼れる武装に戻す |
| ジェノサイド・ショットガン | 威力 ×1.5 | 原作で強い技として有名だったため |
| エア・タックル | 最低値を表示威力の 70% ちょうど | 全体の調整だけでは、わずかに強すぎたため |
| ダブルセイバー | 全段の最低値を表示威力の 66% 以上 | 原作で弱すぎた。コンボ終盤で振るしか用途がないので底上げ |
| 青龍刀 | 全段の最低値を表示威力の 50% 以上 | 原作で弱すぎた。終盤向きだが、上昇の慣性を活かす使い方もできるので控えめに底上げ |

---

## English

### Overview

This mod adds **Tooru**, the mech from BFE, as a playable mech in BSX.

* On the mech select screen, Tooru is placed in Seiran's position.
* All of Tooru's weapons are ported: the 63 normal weapons of BFE (Lv3 only), the 21 Force Crushes (FC), and "Marker Missile", an unused hidden weapon left in the BFE data.
* Visuals, effects and sound effects come from BFE.

### Warnings

> [!WARNING]
> * **Back up your save data before installing.**
> * Tooru's moves will keep being tuned in future updates, so replays that use Tooru will not play back correctly after an update.

### Installation

1. Download the latest `Update3.pac` from [Releases](../../releases) and put it in your BSX install folder (where `BaldrSky.exe` is).
2. If other mods or files there might conflict with it, move them out of the folder.

To uninstall, just delete the `Update3.pac` you added.

### Known issues

* Mega Boost Upper's hit count differs from BFE.
* Stun Rod's sound effect overlaps.
* Taka Otoshi (鷹落とし) has several bugs.

### What was ported

Almost everything is ported as it is in BFE; only a few parts are deliberately tuned differently.

#### Ported as in BFE

* **Movement and formulas**: BFE and BSX differ completely in physics and in their damage and combo-scaling formulas. Instead of eyeballing values, we studied both games' formulas and mapped Tooru's BFE movement and damage onto BSX's.
* **Power**: converted to the same scale as BSX's Kou (e.g. BFE's Arm Jab ≈ Kou's Jab). The strength accounts for BSX's rule that player mechs other than Kou get 1.5x power.
* **Combo scaling**: each weapon is given Kou's values so that it plays a role close to the one it had in BFE (good as a combo starter, good late in a combo, and so on).

#### Tuned differently from BFE

**Dashes**

* Boost dash: BFE has none, so it was added as a new action, a dodge rather than a way to travel.
* Normal dash (regular movement): BFE's dash is fast, so it was set to a speed that works as BSX's regular movement.
* Search dash: BFE's dash has no wind-up, so the search dash reaches full speed immediately.

**Damage (overall)**

* The minimum damage (the floor reached late in a combo) is recalculated while keeping each move's role from BFE. As a guide, before using the Initializer the damage is slightly below BFE, and a full combo with the Initializer does about 2x BFE.
* All FCs have a minimum damage of at least 80% of their displayed power. In BSX, an FC after the Initializer resets scaling to 50%; this rescues them so they still feel satisfying.

**Weapons tuned individually**

| Weapon | Change | Intent |
|---|---|---|
| Drill (ドリル) | Minimum ≥ 100% of displayed power | Its description says it resists scaling; make it reliable late in a combo again |
| Genocide Shotgun (ジェノサイド・ショットガン) | Power x1.5 | It was famous as a strong move in BFE |
| Air Tackle (エア・タックル) | Minimum exactly 70% of displayed power | Slightly too strong with the overall change alone |
| Double Saber (ダブルセイバー) | Minimum of every hit ≥ 66% of displayed power | Too weak in BFE; it is only useful late in a combo, so raise it |
| Seiryuto (青龍刀) | Minimum of every hit ≥ 50% of displayed power | Too weak in BFE; suited to late combos but also usable for its upward momentum, so a modest raise |

---

## 免責事項 / Disclaimer

本 MOD は非公式のファンメイド作品であり、原作の開発元および関係各社とは一切関係ありません。BSX・BFE および本 MOD に含まれる原作の画像・効果音などの著作権は、各権利者に帰属します。本 MOD の使用は自己責任でお願いします。使用によって生じたいかなる損害（セーブデータの破損を含む）についても、作者は責任を負いません。権利者からの申し立てがあった場合は、速やかに公開を停止します。

This mod is an unofficial fan-made work and is not affiliated with the original developer or any related company. BSX, BFE, and the original images, sound effects and other assets included in this mod belong to their respective rights holders. Use this mod at your own risk. The author is not responsible for any damage caused by its use, including corrupted save data. If a rights holder objects, distribution will be stopped promptly.
