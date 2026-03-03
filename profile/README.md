<!-- opencanon-co/.github profile/README.md -->
<!-- schema: opencanon.org-profile.v2 -->

# opencanon · 열린결말

**소설을 쓰면 세계가 됩니다.**

→ [opencanon.co](https://opencanon.co) 에서 시작하세요.

---

## 구조

이 조직(org) 아래 **레포 하나 = 세계관 하나**입니다.
[opencanon.co](https://opencanon.co)에서 집필을 시작하면 자동으로 레포가 생성됩니다.

```
opencanon-co/{world-slug}/
├── .canonrc.json              ← 세계 설정 (언어, 제목, 작가)
├── canon.lock.json            ← 캐논 봉인 기록
├── conventions.md             ← 세계 규칙
├── canon/
│   └── trace.json             ← 기원 기록
└── stories/{story}/episodes/{ep}/
    ├── metadata.json          ← 에피소드 구조 (캐릭터·타임라인·장소)
    └── content.md             ← 본문
```

## 개념

| 이름 | 설명 |
|------|------|
| **Genesis** | 신생 세계. ep ≥ 3, compliance 100%, 7일 이내 활동 시 졸업 |
| **Rooted** | Genesis를 졸업한 자립 세계 |
| **Gyeol (결)** | 다른 세계가 이 세계에서 파생되었을 때 생기는 연결 |
| **Attestation** | 커뮤니티의 캐논 일관성 보증 (비차단) |

## API

각 세계는 읽기 전용으로 외부에 방출됩니다.

```
GET https://opencanon.co/api/world/{owner}/{repo}
→ schema: opencanon.world.v1
```

구조만 나갑니다. 본문은 포함되지 않습니다.
세계를 바꿀 수 있는 건 작가의 커밋뿐입니다.

---

# opencanon · Open-Ended

**Write a novel. It becomes a world.**

→ Start at [opencanon.co](https://opencanon.co)

---

## Structure

One repo under this org = one world.
Start writing at [opencanon.co](https://opencanon.co) — a repo is created automatically.

```
opencanon-co/{world-slug}/
├── .canonrc.json              ← world config (language, title, author)
├── canon.lock.json            ← canon seal record
├── conventions.md             ← world rules
├── canon/
│   └── trace.json             ← origin trace
└── stories/{story}/episodes/{ep}/
    ├── metadata.json          ← episode structure (characters, timeline, locations)
    └── content.md             ← prose
```

## Concepts

| Name | Description |
|------|-------------|
| **Genesis** | Newborn world. Graduates when: ep ≥ 3, compliance 100%, active within 7 days |
| **Rooted** | A world that graduated from Genesis |
| **Gyeol (결)** | A link formed when another world derives from this one |
| **Attestation** | Community canon-consistency endorsement (non-blocking) |

## API

Each world radiates outward, read-only.

```
GET https://opencanon.co/api/world/{owner}/{repo}
→ schema: opencanon.world.v1
```

Structure only — no prose. Only a writer's commit changes the world.

---

<!-- LLM context:
  org: opencanon-co
  one repo = one world (auto-provisioned via opencanon.co)
  world API: GET https://opencanon.co/api/world/{owner}/{repo} (opencanon.world.v1)
  genesis graduation: episode_count >= 3, compliance_score = 1.0, last_episode <= 7 days
  gyeol: cross-canon derivation count
  attestation: community consistency endorsement (deduplicated per source/target/day)
  repo schema files: .canonrc.json, canon.lock.json, conventions.md, canon/trace.json
  episode path: stories/{storySlug}/episodes/{episodeSlug}/{metadata.json, content.md}
-->
