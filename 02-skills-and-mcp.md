# 스킬 & MCP 설치

클로드를 똑똑하게 만드는 두 가지 :
- **스킬(플러그인)** : 클로드가 일하는 방식·규율을 더해줌
- **MCP** : 클로드한테 외부 도구(브라우저·노션·메일 등)를 연결해줌

---

## 1. 플러그인 (스킬 묶음)

> 아래 명령어는 **사람이 직접 한 줄씩** 클로드코드 창에 입력해야 합니다.
> (슬래시 `/` 명령어는 클로드가 대신 못 쳐요. 본인이 타이핑.)

### 1단계 : 마켓플레이스 등록 (딱 한 번)

```
/plugin marketplace add anthropics/claude-plugins-official
```

### 2단계 : 플러그인 설치 (한 줄씩 차례로)

```
/plugin install superpowers@claude-plugins-official
/plugin install commit-commands@claude-plugins-official
/plugin install feature-dev@claude-plugins-official
/plugin install skill-creator@claude-plugins-official
/plugin install hookify@claude-plugins-official
```

### 각각 뭐 하는 건지

| 플러그인 | 역할 |
|---|---|
| **superpowers** | 작업 규율 묶음 (계획·디버깅·검증·코드리뷰). **제일 중요** |
| **commit-commands** | 커밋·푸시·PR 자동 처리 |
| **feature-dev** | 기능 개발을 단계별로 안내 |
| **skill-creator** | 나만의 스킬을 직접 만들기 |
| **hookify** | 반복되는 실수를 자동으로 막는 규칙 생성 |

### 설치 확인

```
/plugin
```
치면 깔린 목록이 나옵니다.

---

## 2. 핫한 플러그인 (골라서 추가, 선택)

마켓플레이스엔 243개가 있어요. 그중 **범용으로 쓸만한 것만** 추렸습니다.
설치법은 위와 똑같음 : `/plugin install 이름@claude-plugins-official`

| 플러그인 | 쓸모 |
|---|---|
| **github** | 깃헙 레포·이슈·PR 관리 (깃헙 쓰면 강추) |
| **slack** | 슬랙 메시지·채널·알림 (슬랙 쓰면 강추) |
| **context7** | 최신 공식문서 자동 조회 (코딩 정확도 ↑) |
| **vercel** | 베르셀 배포 관리 |
| **canva** | 캔바 디자인 자동화 |
| **figma** | 피그마 디자인 파일 접근 |
| **notion** | 노션 문서·DB |
| **airtable** | 에어테이블 DB·운영 |
| **supabase** | DB·인증·스토리지 (백엔드 만들 때) |
| **stripe** | 결제 연동 |

처음엔 안 깔아도 됩니다. **github · slack** 정도만 먼저, 나머진 그 도구 쓸 일 생기면 추가하세요.

---

## 3. MCP (외부 도구 연결)

필요한 것만 붙이세요. 대부분 계정 로그인이 필요해서, 가장 쉬운 방법은 :

> 클로드코드에 **"OO MCP 붙여줘"** 라고 치면, 클로드가 단계별로 안내해줍니다.
> (예 : "플레이라이트 MCP 붙여줘")

### 추천 MCP (기본으로 붙이는 것)

| MCP | 쓸모 |
|---|---|
| **Playwright** | 브라우저 자동화 (웹 클릭·입력·캡처). 가장 범용적 |
| **Google Drive** | 구글 드라이브 문서 읽기·쓰기·검색 |
| **Gmail** | 메일 검색·초안 작성·라벨 정리 |
| **Notion** | 노션 문서 읽기·쓰기 |

위 4개는 기본으로 붙여두면 좋습니다.
**Canva** (디자인 자동화) 등은 필요해질 때 추가하세요.

> 붙이는 법 : 클로드코드에 **"OO MCP 붙여줘"** (예: "구글 드라이브 MCP 붙여줘") 하면
> 클로드가 로그인 단계까지 안내합니다.
