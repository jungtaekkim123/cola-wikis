# Wiki Schema

## Domain
개인 연구·학습 지식베이스. 주로 **AI/ML 리서치**(논문·모델·기법)와 **수학 공부**(정리·증명·개념)를
다루며, 그 외 인접 기술 주제로 확장 가능. 소스는 사람이 큐레이션하고, 에이전트가 요약·교차참조·정리한다.

## Conventions
- File names: lowercase, hyphens, no spaces (e.g., `transformer-architecture.md`)
- Every wiki page starts with YAML frontmatter (see below)
- Use `[[wikilinks]]` to link between pages (minimum 2 outbound links per page)
- When updating a page, always bump the `updated` date
- Every new page must be added to `index.md` under the correct section
- Every action must be appended to `log.md`
- **Provenance markers:** On pages that synthesize 3+ sources, append `^[raw/articles/source-file.md]`
  at the end of paragraphs whose claims come from a specific source. Optional on single-source pages
  where the `sources:` frontmatter is enough.
- 수학 페이지는 LaTeX을 `$...$`(인라인) / `$$...$$`(블록)로 작성 — Obsidian에서 그대로 렌더된다.

## Frontmatter
```yaml
---
title: Page Title
created: YYYY-MM-DD
updated: YYYY-MM-DD
type: entity | concept | comparison | query | summary
tags: [from taxonomy below]
sources: [raw/articles/source-name.md]
# Optional quality signals:
confidence: high | medium | low        # how well-supported the claims are
contested: true                        # set when the page has unresolved contradictions
contradictions: [other-page-slug]      # pages this one conflicts with
---
```

`confidence` / `contested` are optional but recommended for opinion-heavy or fast-moving topics.
Lint surfaces `contested: true` and `confidence: low` pages so weak claims don't harden into fact.

### raw/ Frontmatter
Raw sources ALSO get a small frontmatter block so re-ingests can detect drift:

```yaml
---
source_url: https://example.com/article   # original URL, if applicable
ingested: YYYY-MM-DD
sha256: <hex digest of the raw content below the frontmatter>
---
```

`sha256:` lets a future re-ingest skip unchanged content and flag drift. Compute over the body only.

## Tag Taxonomy
모든 페이지의 태그는 아래 목록에 있어야 한다. 새 태그가 필요하면 **먼저 여기 추가한 뒤** 사용한다 (tag sprawl 방지).

**AI/ML — Models & Systems**
- `model` `architecture` `benchmark` `training` `inference` `dataset`

**AI/ML — Techniques**
- `optimization` `fine-tuning` `rl` `alignment` `evaluation` `prompting` `agents` `rag`

**Mathematics**
- `set-theory` `linear-algebra` `analysis` `probability` `statistics` `optimization-theory` `topology`
- `theorem` `proof` `definition` `foundations`
  - `foundations`: 공리적 토대·논리적 미묘함 (선택공리, 산술의 기본정리, 정렬성 등 "공리적 비약" 지점)

**People / Orgs / Sources**
- `person` `lab` `company` `paper` `book` `course`

**Meta**
- `comparison` `timeline` `open-question` `prediction` `study-note` `controversy`

> 참고: ML 최적화 기법은 `optimization`, 수학 최적화 이론은 `optimization-theory`로 구분한다.

## Page Thresholds
- **Create a page** when an entity/concept appears in 2+ sources OR is central to one source
- **Add to existing page** when a source mentions something already covered
- **DON'T create a page** for passing mentions, minor details, or things outside the domain
- **Split a page** when it exceeds ~200 lines — break into sub-topics with cross-links
- **Archive a page** when fully superseded — move to `_archive/`, remove from index

## Entity Pages
One page per notable entity (model, person, lab, paper, book). Include: overview, key facts/dates,
relationships ([[wikilinks]]), source references.

## Concept Pages
One page per concept/topic (a technique, a theorem, a definition). Include: definition/explanation,
current state of knowledge, open questions/debates, related concepts ([[wikilinks]]).
수학 개념 페이지는 가능하면 *Statement → Intuition → Proof sketch → Examples* 순으로.

## Comparison Pages
Side-by-side analyses. Include: what's compared and why, dimensions (table preferred),
verdict/synthesis, sources.

## Update Policy
When new information conflicts with existing content:
1. Check the dates — newer sources generally supersede older ones
2. If genuinely contradictory, note both positions with dates and sources
3. Mark the contradiction in frontmatter: `contradictions: [page-name]`
4. Flag for user review in the lint report
