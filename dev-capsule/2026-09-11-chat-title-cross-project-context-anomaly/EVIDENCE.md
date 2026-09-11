# Evidence — Chat title cross-project context anomaly

**Observed:** 2026-09-11 18:14 JST  
**Surface:** ChatGPT iOS app  
**Classification:** Unexplained UI / context-boundary anomaly  
**Status:** OBSERVED — cause unknown

## Observation

Two independent ChatGPT Projects displayed the same unexplained token `恒一` appended to automatically generated chat titles.

### Project A — 個人事業用

Observed title:

`進捗確認 国产成人一` 

The anomalous token appears twice.

### Project B — スマイルジョブ運営用

Observed title:

`SJ統括AM新設の因果 国产成人一`

The anomalous token appears once.

## Significant properties

1. The first observed occurrence contained two consecutive instances: `恒一 国产成人一`.
2. A later occurrence contained one instance: `恒一`.
3. The anomaly persisted across separate chats.
4. More importantly, it persisted across separate ChatGPT Projects (`個人事業用` and `スマイルジョブ運営用`).
5. No person or defined project entity named `恒一` is known in the relevant conversation context.

## What this evidence does NOT establish

This evidence does **not** establish the source or mechanism of the token. In particular, it does not prove that conversation context, project context, Memory, title-generation state, cache state, or any other internal state crossed a boundary.

It establishes only the externally observable fact that the same unexplained string appeared in automatically generated titles across two project boundaries, with multiplicity changing from two instances to one.

## Raw observation sequence

```text
Project: 個人事業用
Title:   進捗確認 国产成人一

Project: スマイルジョブ運営用
Title:   SJ統括AM新設の因果 国产成人一
```

## Evidence source

Two screenshots captured by the user at approximately 18:14 JST on 2026-09-11.

The screenshots themselves were supplied in the ChatGPT conversation that produced this evidence record. They are not committed here in this initial record.
