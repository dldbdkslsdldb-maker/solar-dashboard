# ☀️ 신신사 태양광발전소 실적 현황

신신사(주) 창원2공장 옥상 태양광발전소 대표이사 업무보고용 실적 대시보드

---

## 📁 파일 구조

shinshin-solar-dashboard/

│

├── data/

│   └── solar\_data.json          ← ✅ 매월 이 파일만 수정

│

├── 신신사 태양광발전소 실적현황\_v2.html  ← 대시보드 본체 (수정 불필요)

│

└── README.md

---

## 🔄 월간 업데이트 방법

### 1\. `solar_data.json` 열기

data/solar\_data.json

### 2\. `_last_updated` 수정

"\_last\_updated": "2026-07"

### 3\. `monthly` 배열에 신규 월 추가 (맨 뒤에 append)

{

  "month": "7월",

  "generation\_kwh": 118000,

  "trade\_kwh": 117200,

  "smp\_unit": 117.5,

  "rec\_unit": 54.5,

  "smp\_revenue": 13771250,

  "rec\_revenue": 6387440,

  "total\_revenue": 20158690,

  "cost": 980000,

  "net\_income": 19178690

}

### 4\. GitHub 업로드 (2가지 방법)

**방법 A \- GitHub 웹에서 직접 편집 (권장 · 간편)**

1. 저장소 접속 → `data/solar_data.json` 클릭  
2. 우측 상단 ✏️ (Edit) 버튼 클릭  
3. 내용 수정 후 **Commit changes** 클릭

**방법 B \- Git 명령어**

git add data/solar\_data.json

git commit \-m "2026-07 실적 업데이트"

git push

---

## 🌐 GitHub Pages 배포 방법

1. 저장소 → **Settings** → **Pages**  
2. Source: `Deploy from a branch`  
3. Branch: `main` / `/ (root)` 선택 → **Save**  
4. 약 1\~2분 후 URL 생성: `https://{계정명}.github.io/shinshin-solar-dashboard/신신사 태양광발전소 실적현황_v2.html`

---

## 📊 대시보드 구성

| 영역 | 항목 |
| :---- | :---- |
| **상단 KPI** | 총 매출액, SMP 수익, REC 수익, 당기순이익, 누적 계획 달성률 |
| **중단 차트** | 월별 매출, SMP\&REC 단가 추이, 발전량&거래량, 누적 계획대비 실적, 손익 추이, 원가 구성 |
| **하단 테이블** | 손익계산서 (월별/누적/계획/달성률) |

---

## 🔧 수정이 필요한 초기 설정값

`solar_data.json` 내 아래 항목을 실제 값으로 교체하세요.

| 항목 | 경로 | 설명 |
| :---- | :---- | :---- |
| 설비 용량 | `meta.capacity_kw` | 실제 발전 용량(kW) |
| 준공일 | `meta.install_date` | YYYY-MM 형식 |
| 연간 매출 계획 | `plan.annual_revenue` | 원 단위 |
| 원가 구성 | `cost_breakdown` | 감가상각 등 연간 금액 |
| 월별 실적 | `monthly[]` | 월별로 추가 |

---

## 📞 관리

- **담당**: 신신사(주) 총무팀  
- **보고 주기**: 월 1회 (익월 초 업데이트)

