# Athena_99 (athena_99_sekirei)

A M.U.G.E.N character based on **Athena Asamiya** from *The King of Fighters '99* (KOF'99).

---

## Character Introduction

### Character Name
**Athena Asamiya** — Display name: Athena_99

### Original Creator
**sekirei**

### Character Storyline
Athena Asamiya is a psychic idol from SNK's *The King of Fighters* series. She first appeared in *Psycho Soldier* (1986) and has been a recurring character in the KOF franchise. In KOF'99, Athena fights as part of the "Psycho Soldier" team alongside Sie Kensou and Bao. She uses her psychic powers for both offensive and defensive techniques, combining martial arts with supernatural abilities. Her signature moves include the Phoenix Arrow (psychic arrow), Psychic Ball, and Shining Crystal Bit.

### Version Information
- **MUGEN Version:** 04,14,2002
- **Character Base:** KOF'99 (The King of Fighters 1999)
- **Platform:** Windows MUGEN

---

## Documentation Index

| Document | Description |
|----------|-------------|
| [docs/TRANSLATION.md](docs/TRANSLATION.md) | Japanese-to-English translation table for all CNS, CMD, and DEF file comments |
| [docs/log.md](docs/log.md) | Creator development history and version changelog |

---

## System Architecture

### File Structure

| File | Purpose |
|------|---------|
| `athena_99_sekirei.def` | Character definition and file references |
| `athena_99-cmd.cns` | Command definitions and state -1 (global) controllers |
| `athena_99-D.cns` | Character data (life, power, velocity, size) |
| `athena_99-N.cns` | Normal states (stands, crouches, taunts) |
| `athena_99-C.cns` | Common states (stunnedef 0, 10, physics) |
| `athena_99-S.cns` | Standing states |
| `athena_99-H.cns` | Crouching states |
| `athena_99-E.cns` | Air states |
| `athena_99-2.cns` | Additional state definitions |
| `athena_99-3.cns` | AI and system configuration |
| `athena_99-sys.cns` | System states (stun, crush, team mode) |
| `!!!config.txt` | Config helper (Statedef 8888) |

### Fight Mode Architecture

#### Basic States (State Numbers)
- **Stand (S):** 200, 205, 210, 215, 230, 235, 240, 245
- **Crouch (C):** 400, 410, 430, 440
- **Air (A):** 600, 605, 610, 615, 630, 635, 640, 645
- **Recovery:** 216 (counter hit)

#### Special Move States (1000–1999)
| State | Move | Command |
|-------|------|---------|
| 1000/1050 | Phoenix Arrow (close/far) | 214x / 214y |
| 1100/1150 | Psycho Sword | 623x / 623y |
| 1200/1250 | Psycho Reflector | 214a / 214b |
| 1300/1350 | Psycho Ball (ground/air) | 41236x / 41236y |
| 1400/1450 | Shining Crystal Bit | 236a / 236b |
| 1500–1570 | Psychic Throw variants | 236a / 236b (ground/air) |

#### Super Move States (3000–3250)
| State | Super | Power Cost |
|-------|-------|------------|
| 3000 | LV1 Psycho Ball Super | 1000+ |
| 3050 | LV2 Psycho Ball Super | 3000+ (2000 in team) |
| 3200 | LV1 Shining Crystal Bit (air) | 1000+ |
| 3250 | LV2 Shining Crystal Bit (air) | 3000+ |

#### System States
- **Run:** 100 (FF), 105 (BB)
- **Recovery:** 107, 108, 109, 110, 112
- **Throw:** 700, 710, 750
- **Counter Throw:** 280, 285, 680
- **Taunt:** 195

### Skill System

#### Special Moves (Detailed)
| Skill | State(s) | Command | Description |
|-------|----------|---------|--------------|
| Phoenix Arrow | 1000, 1050 | 214x, 214y | Psychic projectile; close (x) vs far (y) versions |
| Psycho Sword | 1100, 1150 | 623x, 623y | Dragon-punch style slash; ground and air cancelable |
| Psycho Reflector | 1200, 1250 | 214a, 214b | Reflects projectiles; spawns helper ID 1200/1250 |
| Psycho Ball | 1300, 1350 | 41236x, 41236y | Charge forward projectile; ground (1300/1350) and air variants |
| Shining Crystal Bit | 1400, 1450 | 236a, 236b | Crystal projectile; spawns helper for projID 1400 |
| Psychic Throw | 1500–1570 | 236a, 236b | Teleport grab; ground (1500/1550) and air (1510/1560) |

#### Super Moves (Detailed)
| Super | State(s) | Command | Power | Notes |
|-------|----------|---------|-------|-------|
| Psycho Ball Super LV1 | 3000 | 6321463214x/y | 1000 | Ground/air; SC cancelable |
| Psycho Ball Super LV2 | 3050 | 6321463214xy/c | 3000 (2000 team) | Max mode; bit helpers 3070/3071 |
| Shining Crystal Bit LV1 | 3200 | 236236a/b | 1000 | Air only |
| Shining Crystal Bit LV2 | 3250 | 236236ab/c | 3000 (2000 team) | Air only; clone helpers 3220–3224 |

#### Command Inputs (Numpad Notation)
- **6321463214** — Half-circle back ×2 + button (LV1/LV2 Psycho Ball Super)
- **236236** — Double quarter-circle forward (Shining Crystal Bit, air)
- **623** — Dragon punch (Psycho Sword)
- **41236** — Charge forward (Psycho Ball)
- **214** — Charge back (Phoenix Arrow, Psycho Reflector)
- **236** — Quarter-circle forward (Psychic Throw, Shining Crystal Bit)

### Animation Counterpart Mapping

| Animation Type | States | Notes |
|----------------|--------|-------|
| Far stand X/Y/A/B | 200, 210, 230, 240 | Light attacks |
| Close stand X/Y/A/B | 205, 215, 235, 245 | Proximity-based (P2bodydist) |
| Crouch X/Y/A/B | 400, 410, 430, 440 | Low attacks |
| Air X/Y/A/B (neutral) | 600, 610, 630, 640 | vel X = 0 |
| Air X/Y/A/B (moving) | 605, 615, 635, 645 | vel X ≠ 0 |
| Counter hit recovery | 216 | From stand normals |
| Forward roll | 107 | Recovery option |
| Back roll | 108, 109 | Recovery option |
| Air recovery | 112 | From knockdown (Numexplod 565656) |

### Animation–State Counterparty Reference

| State | Animation | HitDef Element | Cancel Paths |
|-------|-----------|----------------|--------------|
| 200–245 | Stand normals | animelem 2–4 | → 0, 300, 107, 108 |
| 400–440 | Crouch normals | animelem 2–3 | → 11, 107, 108 |
| 600–645 | Air normals | animelem 2–4 | → 52 (land) |
| 1000/1050 | Phoenix Arrow | animelem 5 | Helper 1000/1050, projID 1000 |
| 1100/1150 | Psycho Sword | animelem 3–7 | → 1170 (land) |
| 1200/1250 | Psycho Reflector | animelem 2/5 | Helper 1200/1250, projID 1200 |
| 1300/1350 | Psycho Ball | animelem 3–11 | → 1370 (land) |
| 1400/1450 | Shining Crystal Bit | animelem 4/12 | Helper 1400/1450, projID 1400 |
| 1500–1570 | Psychic Throw | animelem 5–8 | Helper 1500, TargetBind |

### Variable Usage (Key Vars)
- **var(6):** System mode (400 = team mode)
- **var(18):** Super mode (0=normal, 1=SC, 2=DC)
- **var(28):** Helper/partner flag
- **var(59):** AI level
- **var(47):** Enemy target ID
- **var(36):** Chain throw / combo flag
- **var(3):** Trip guard flag (Crouch B knockdown)

### Projectile and Helper IDs
| ID | Source | Type |
|----|--------|------|
| 1000 | Phoenix Arrow (1000/1050) | Projectile |
| 1200 | Psycho Reflector (1200/1250) | Projectile |
| 1400 | Shining Crystal Bit (1400/1450) | Projectile |
| 1500 | Psychic Throw helper | Helper (tama) |
| 3070/3071 | Psycho Ball Super bits | Helper (bit-Main, bit-Sub) |
| 3220–3224 | Shining Crystal Bit clones | Helper (bunshin) |

---

## License

**Creative Circle License**

This character is an edit/adaptation by the original author (sekirei). The character design and assets are derived from SNK's *The King of Fighters* series. This work is shared for non-commercial MUGEN use. Original SNK/CAPCOM/Elecbyte credits apply. See [docs/log.md](docs/log.md) for full acknowledgments.
