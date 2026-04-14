# HIZ Website — Project Memory

> 이 파일은 Claude Code가 프로젝트를 이어받을 때 읽는 컨텍스트 문서다.
> 작업할 때마다 최신 상태로 업데이트한다.

---

## 프로젝트 개요

| 항목 | 내용 |
|---|---|
| 클라이언트 | HIZ (히즈) — 브랜드 에이전시 |
| 목표 | hizsite.com 리뉴얼 (Wix → Vercel) |
| 워크플로우 | Figma MCP → Claude → GitHub → Vercel |
| 런칭 목표 | 2026년 5월 24일 |

---

## 접근 정보

| 항목 | 값 |
|---|---|
| GitHub | https://github.com/FOWARP/hiz-website |
| Vercel | https://hiz-website.vercel.app |
| Figma 파일 | https://www.figma.com/design/SaPaZQtsiAqbAoawELtAFz/HIZ-Website |
| 현재 운영 사이트 | hizsite.com (Wix, 런칭 전까지 유지) |

---

## 페이지 구성 (확정)

| 페이지 | 파일명 | Figma 아트보드 | 상태 |
|---|---|---|---|
| Project | project.html | (PC) Project — node 18:128 | 퍼블리싱 완료 (영상 플레이스홀더) |
| Home | — | (PC) Main — node 3:2 | 미작업 |
| About | — | — | 미작업 |
| Contact | — | — | 미작업 |

---

## 기술 스택

- **HTML/CSS/JS** 순수 바닐라 (프레임워크 없음)
- **폰트**: Pretendard Variable (CDN), Arial
- **배포**: Vercel (GitHub 연동, git push → 자동 배포)
- **스케일링**: 1920px 기준 `transform: scale()` 방식 (모바일 반응형 추후 추가 예정)

---

## 디렉토리 구조

```
hiz-website/
├── PROJECT.md          ← 이 파일 (프로젝트 메모리)
├── project.html        ← Project 페이지
├── media/
│   ├── README.md       ← 영상 파일 컨벤션
│   ├── .gitkeep
│   ├── goventure.mp4   ← (미등록, 추가 대기)
│   └── ...
```

---

## 영상/미디어 컨벤션

**규칙: 피그마 레이어 이름 기반 파일명 (소문자, 공백→하이픈)**

| 피그마 레이어 | 파일명 | 상태 |
|---|---|---|
| Project_Gallery_01_Media | goventure.mp4 | 파일 미등록 |
| Project_Gallery_02_Media | starbucks.mp4 | 파일 미등록 |

영상 추가 방법:
```bash
cd ~/hiz-website
git add media/파일명.mp4
git push
```

---

## 완료 작업 이력

| 날짜 | 작업 |
|---|---|
| 2026-04-14 | project.html 퍼블리싱, GitHub/Vercel 세팅 완료 |
| 2026-04-14 | /media/ 폴더 컨벤션 수립, video 태그 연결 |

---

## 디자인 스펙 (Figma 기준)

- **기준 해상도**: 1920×1080px (16:9)
- **좌우 여백**: 60px
- **헤더**: top 20px, height 59px, border-radius 22px, backdrop blur
- **본문 시작**: top 199px
- **갤러리 미디어**: 895×504px (16:9), gap 10px
- **갤러리 행 간격**: 40px
- **배경색**: #fff
- **텍스트 컬러 메인**: #000
- **텍스트 컬러 서브**: #999796

---

## 주의사항

- Figma MCP 에셋 URL (`figma.com/api/mcp/asset/...`) 은 **7일 후 만료**됨 → 최종 빌드 전 자체 호스팅 필요
- 헤더 로고, 화살표 아이콘 등 Figma 에셋 URL 사용 중 → 만료 전 `/media/` 또는 `/assets/`에 옮길 것
- git committer 정보 미설정 → `git config user.name / user.email` 설정 권장
