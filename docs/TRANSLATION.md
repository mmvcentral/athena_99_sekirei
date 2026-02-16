# Translation Table

Japanese-to-English translations for comments in CNS, CMD, and DEF files.

---

## DEF File (athena_99_sekirei.def)

| Original (Japanese/Code) | English |
|--------------------------|---------|
| 賗ðQÆ (versiondate) | Version date |
| パレット関連 | Palette related |

---

## CMD File (athena_99-cmd.cns)

### Command Section Headers
| Original | English |
|----------|---------|
| AI | AI |
| 必殺・技 | Special Move / Skill |
| 技 | Skill |
| Double Tap | Double Tap |
| 2/3 Button Combination | 2/3 Button Combination |
| Hold button | Hold button |
| Hold Dir | Hold Direction |
| ボタン指定（離さない） | Button input (without release) |

### State Comments
| Original | English |
|----------|---------|
| くう２・れば | LV2 Super |
| くう１・れば | LV1 Super |
| くう２・シャイン | LV2 Shining (air) |
| くう１・シャイン | LV1 Shining (air) |
| スラッシュ | Psycho Sword |
| バスター | Psycho Ball |
| リフレクター | Psycho Reflector |
| テレポート | Teleport |
| 投げ・テレ | Psychic Throw |
| 基本--基本---- | Basic--Basic---- |
| 連続 | Chain/Combo |
| 取消--地上技-- | Cancel--Ground skill-- |
| 取消--テレ技-- | Cancel--Tele skill-- |
| 取消--SC-- | Cancel--Super Cancel-- |
| キー | Guard |
| ダッシュ | Dash |
| バックダッシュ | Back dash |
| しゃがみ | Crouch |
| 回転投げ | Counter throw |
| 回転投げ^連続投げ | Counter throw ^ Chain throw |
| テレ技 | Teleport recovery |
| 通常技 | Normal recovery |
| 通常技(XX|fb) | Normal recovery (XX\|fb) |
| AC通常技 | AC Normal recovery |
| 起き上がり | Wake-up |
| 前転 | Forward roll |
| 後転 | Back roll |
| 投げ | Throw |
| 連続投げ | Chain throw |
| 起き上がり投げ | Wake-up throw |
| 反転 | Turn around |
| 端越え | Edge climb |
| しゃがみ | Crouch |
| 近立X/Y/A/B | Close stand X/Y/A/B |
| 遠立X/Y/A/B | Far stand X/Y/A/B |
| しゃがみX/Y/A/B | Crouch X/Y/A/B |
| 空中X/Y/A/B | Air X/Y/A/B |
| しゃがみ投げ | Crouch throw |
| 空中投げ | Air throw |
| 挑発 | Taunt |

---

## CNS Files - Common Terms

### athena_99-D.cns
| Original | English |
|----------|---------|
| キャラ^通常技 | Character ^ Normal skill |
| ライフ | Life |
| パワー | Power |
| 攻撃力 | Attack power |
| 防御力 | Defense |
| 連続 | Chain |
| しゃがみ | Crouch |
| 前進 | Forward |
| 後退 | Back |
| 前ダッシュ | Forward dash |
| 後ダッシュ | Back dash |
| 中立ジャンプ | Neutral jump |
| 後ジャンプ | Back jump |
| 前ジャンプ | Forward jump |
| 後ダッシュ後ジャンプ | Back dash back jump |
| 前ダッシュ後ジャンプ | Forward dash back jump |
| 2回ジャンプ以降 | 2nd jump onward |
| 横倍率 | Horizontal scale |
| 縦倍率 | Vertical scale |
| 当たり判定の幅 | Hitbox width |
| 重力 | Gravity |
| 摩擦係数 | Friction coefficient |

### athena_99-N.cns
| Original | English |
|----------|---------|
| キャラ^通常技 | Character ^ Normal skill |
| 待機 | Idle |
| やったー | "Yatta!" (taunt) |
| ふふふ | "Fufufu" (taunt) |
| アテナに会わせ | "Meet Athena" (taunt) |
| vs99ぱい | vs Bao |
| vs99ぷれ | vs Kensou |
| 本家アテナ | Original Athena |
| 本家アテナ^ | Original Athena ^ |

### athena_99-C.cns
| Original | English |
|----------|---------|
| 共通 | Common |
| 通常攻撃 | Normal attack |
| 投げ判定 | Throw判定 |
| ダッシュ判定 | Dash判定 |
| 前転 | Forward roll |
| 後転 | Back roll |

### athena_99-sys.cns
| Original | English |
|----------|---------|
| XIシステム | XI System |
| 技判定・取消^ゲージ^ super^DC^ジャンプ^スト^キー | Skill判定・Cancel ^ Gauge ^ Super ^ DC ^ Jump ^ Stand ^ Guard |
| 攻撃攻撃・キー管理 | Attack・Guard management |
| 攻撃・キー | Attack・Guard |
| 攻撃・1最高 | Attack・1 max |
| 攻撃・2最高 | Attack・2 max |
| 攻撃・3最高 | Attack・3 max |
| 攻撃・4最高 | Attack・4 max |
| 攻撃・5最高 | Attack・5 max |
| 攻撃・6最高 | Attack・6 max |
| 攻撃・7最高 | Attack・7 max |
| 攻撃・8最高 | Attack・8 max |
| 攻撃・9最高 | Attack・9 max |
| 攻撃・10最高 | Attack・10 max |

---

## 詳細.txt (Details) - Translated Content

Source: 詳細.txt (character details document)

### Frame Data
- **近立 (Close stand):** 12 frames guard, 9 frames hit
- **遠立 (Far stand):** 10 frames guard, 13 frames hit
- **しゃがみ (Crouch):** 10 frames guard, 13 frames hit

### State Reference
- 近立X/Y/A/B → 205, 215, 235, 245
- 遠立X/Y/A/B → 200, 210, 230, 240
- しゃがみX/Y/A/B → 400, 410, 430, 440
- 空中X/Y/A/B → 600, 610, 630, 640

---

## アテナ99一覧.txt (Athena 99 List) - Key Terms

| Original | English |
|----------|---------|
| 遠立 | Far stand |
| 近立 | Close stand |
| しゃがみ | Crouch |
| 空中 | Air |
| 打ち切り | Cancel |
| 投げ | Throw |
| ダッシュ | Dash |
| バックダッシュ | Back dash |
| 起き上がり | Wake-up |
| 回転投げ | Counter throw |
| しゃがみ投げ | Crouch throw |
| 空中投げ | Air throw |
| 挑発 | Taunt |
| くう１・れば | LV1 Super |
| くう２・れば | LV2 Super |
| くう１・シャイン | LV1 Shining |
| くう２・シャイン | LV2 Shining |
| スラッシュ | Psycho Sword |
| バスター | Psycho Ball |
| リフレクター | Psycho Reflector |
| テレポート | Teleport |
| 投げ・テレ | Psychic Throw |

---

## アテナ99りどみ.txt (Athena 99 Rhythm) - Key Terms

| Original | English |
|----------|---------|
| 本家 アテナ-KOF'99 | Original Athena KOF'99 |
| 攻撃 | Attack |
| 技 | Skill |
| 投げ | Throw |
| 通常技 | Normal skill |
| 必殺技 | Special move |
| 超必殺技 | Super special move |
| キャンセル | Cancel |
| 連続 | Chain |
| 地上 | Ground |
| 空中 | Air |
| しゃがみ | Crouch |
| 近立 | Close stand |
| 遠立 | Far stand |
