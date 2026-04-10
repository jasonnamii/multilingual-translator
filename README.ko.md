# 다국어 번역 운영 도구

> 🇺🇸 [English README](./README.md)

**구조화된 .md 문서의 다국어 번역 및 구조 일치 QC 검증입니다.**

## 사전 요구사항

- **Obsidian Vault** — QC 검증 스크립트가 구조 보존을 위해 위키링크(`[[...]]`)와 임베드(`![[...]]`)를 계산함
- **Claude Cowork 또는 Claude Code** 환경

## 목적

multilingual-translator는 다국어 출판을 자동화합니다: English를 기준으로 설정하고, 병렬로 번역하며, 콜아웃, 표, 위키링크, HTML div에 걸쳐 구조 보존을 검증합니다.

## 사용 시점 및 방법

구조화된 .md 문서를 번역해야 할 때 발동합니다. 항상 English로 먼저 번역하고(기준), 그 다음 다른 언어들을 병렬로 번역합니다. 모든 번역 후 구조적 동등성을 검증합니다.

## 사용 예시

| 상황 | 프롬프트 | 결과 |
|---|---|---|
| 3개 언어로 번역 | `"README를 스페인어, 프랑스어, 독일어로 번역해줘"` | EN 기준→병렬 ES/FR/DE→QC: 구조 일치 확인→3개 번역 파일 |
| 다국어 API 문서 | `"API 문서를 5개 언어로 번역해줘, 코드 블록은 유지"` | EN 버전→코드 펜스 보존→5개 언어→구조 검증 |
| 배치 번역 | `"10개 문서를 일본어, 한국어, 중국어로 번역해줘"` | 서브에이전트 병렬화→각각 독립적으로 검증→커버리지 리포트 |

## 핵심 기능

- English 우선 기준으로 정본 버전 설정
- N개 언어로 동시 병렬 번역
- 구조 일치 QC: 콜아웃, 표, 위키링크, HTML div, 코드 블록 보존
- 병렬 문서 처리를 위한 서브에이전트 관리
- 구조 일치 백분율을 포함한 검증 리포트

## 연관 스킬

- **[deliverable-engine](https://github.com/jasonnamii/deliverable-engine)** — 번역에 이상적인 구조화된 문서
- **[obsidian-markdown](https://github.com/jasonnamii/obsidian-markdown)** — 위키링크가 유지된 Obsidian markdown 번역

## 설치

```bash
git clone https://github.com/jasonnamii/multilingual-translator.git ~/.claude/skills/multilingual-translator
```

## 업데이트

```bash
cd ~/.claude/skills/multilingual-translator && git pull
```

`~/.claude/skills/`에 배치된 스킬은 Claude Code 및 Cowork 세션에서 자동으로 사용할 수 있습니다.

## Cowork 스킬 생태계

25개 이상의 커스텀 스킬 중 하나입니다. 전체 카탈로그: [github.com/jasonnamii/cowork-skills](https://github.com/jasonnamii/cowork-skills)

## 라이선스

MIT 라이선스 — 자유롭게 사용, 수정, 공유하세요.