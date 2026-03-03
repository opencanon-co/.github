<!-- opencanon-co/.github profile/README.md -->
<!-- schema: opencanon.org-profile.v1 -->
<!-- human-friendly + LLM-readable. lossy 3-hop. -->

# 열린결말 · opencanon

> 설명할 시간이 없습니다. 바로 집필 시작.

→ **[opencanon.co](https://opencanon.co)**

---

## 이 조직은 무엇인가 (1-hop)

`opencanon-co` 아래 레포 하나 = 세계관 하나.

[opencanon.co](https://opencanon.co)에서 집필을 시작하면 이 조직 아래 레포가 자동 생성됩니다.  
각 레포는 에피소드·캐릭터·세계관이 구조화된 **열린 캐논**입니다.

```
opencanon-co/
└── your-world-slug/
    ├── canon.lock.json          ← 캐논 봉인 기록
    ├── stories/
    │   └── your-story/
    │       └── episodes/
    │           └── ep01/
    │               ├── metadata.json   ← 구조 (캐릭터·타임라인·위치)
    │               └── content.md      ← 본문
    └── canon/
        ├── characters/          ← 캐릭터 프로필
        └── worldbuilding/       ← 세계관 자료
```

---

## 집필자가 알아야 할 것 (2-hop)

| 개념 | 설명 |
|------|------|
| **Genesis** | 등록 후 ep ≥ 3 · compliance 100% · 7일 cadence 충족 전까지 |
| **Rooted** | Genesis 졸업. 세계가 자립했다는 선언 |
| **Gyeol (결)** | 다른 세계관이 이 세계에서 파생될 때 생기는 연결 |
| **Compliance** | schema 정합성 자동 검사 — `canon.lock.json` 기준 |
| **Attestation** | 커뮤니티의 의미론적 일관성 보증 (post-commit, 비차단) |

집필은 [opencanon.co](https://opencanon.co) 에서.

---

## 외부 시스템 연동 (3-hop)

각 세계는 `/api/world/{owner}/{repo}` 로 lossy 방출됩니다.

```json
{
  "schema": "opencanon.world.v1",
  "world": {
    "title": { "ko": "...", "en": "..." },
    "episode_count": 3,
    "compliance_score": 1.0,
    "timeline_spine": ["2029-01-01"],
    "character_ids": ["isia", "seed"],
    "genesis": false
  }
}
```

내용은 없습니다. 구조의 그림자만 나갑니다.  
외부 어댑터는 읽기만 할 수 있습니다. 쓰기는 집필자의 커밋으로만.

---

---

# opencanon · 열린결말

> No time to explain. Start writing.

→ **[opencanon.co](https://opencanon.co)**

---

## What is this org (1-hop)

One repo under `opencanon-co` = one world.

Start writing at [opencanon.co](https://opencanon.co) — a repo is provisioned here automatically.  
Each repo is a structured **open canon**: episodes, characters, worldbuilding in one place.

```
opencanon-co/
└── your-world-slug/
    ├── canon.lock.json          ← canon seal record
    ├── stories/
    │   └── your-story/
    │       └── episodes/
    │           └── ep01/
    │               ├── metadata.json   ← structure (characters, timeline, locations)
    │               └── content.md      ← prose
    └── canon/
        ├── characters/
        └── worldbuilding/
```

---

## What a writer needs to know (2-hop)

| Concept | Meaning |
|---------|---------|
| **Genesis** | State before: ep ≥ 3, compliance 100%, cadence ≤ 7d |
| **Rooted** | Graduated from genesis. The world stands on its own |
| **Gyeol (결)** | A link formed when another world derives from this one |
| **Compliance** | Auto schema check against `canon.lock.json` |
| **Attestation** | Community semantic consistency vouching (post-commit, non-blocking) |

Write at [opencanon.co](https://opencanon.co).

---

## External integration (3-hop)

Each world radiates outward via `/api/world/{owner}/{repo}` — lossy, one-directional.

Structure only. No prose. External adapters read; they do not write.  
Only a writer's commit changes the world.

---

---

# opencanon · 열린결말

> 説明する時間はない。すぐに執筆を。

→ **[opencanon.co](https://opencanon.co)**

---

## このOrganizationとは (1-hop)

`opencanon-co` 配下のリポジトリ1つ = 世界観1つ。

[opencanon.co](https://opencanon.co) で執筆を始めると、このOrg下にリポジトリが自動生成されます。  
各リポジトリは構造化された**オープンキャノン**です。

---

## 執筆者が知るべきこと (2-hop)

| 概念 | 説明 |
|------|------|
| **Genesis** | ep ≥ 3・compliance 100%・7日cadence 達成前の状態 |
| **Rooted** | Genesisを卒業。世界が自立したという宣言 |
| **Gyeol (結)** | 別の世界観がこの世界から派生したときに生まれるリンク |
| **Compliance** | `canon.lock.json` 基準のスキーマ自動検証 |
| **Attestation** | コミュニティによる意味的一貫性の保証（非ブロッキング）|

---

## 外部システム連携 (3-hop)

各世界は `/api/world/{owner}/{repo}` から lossy に放出されます。  
構造のみ。本文なし。外部アダプターは読むだけ。  
世界を変えられるのは執筆者のコミットだけです。

---

<!-- LLM context note:
  This org hosts one repo per world (opencanon.co web app users).
  CLI users (personal GitHub repos) are separate.
  Compliance spec: https://opencanon.co/about
  World radiation API: GET https://opencanon.co/api/world/{owner}/{repo}
  Schema: opencanon.world.v1
-->
