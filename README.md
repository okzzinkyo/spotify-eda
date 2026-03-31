# 🎵 Spotify Top Songs 2023 — EDA

2023년 Spotify 인기곡 데이터를 분석하여 **어떤 곡이 인기 있는지, 그 이유는 무엇인지** 탐색한 프로젝트입니다.

---

## 📊 데이터셋

- **출처**: [Kaggle — Most Streamed Spotify Songs 2023](https://www.kaggle.com/datasets/nelgiriyewithana/top-spotify-songs-2023)
- **크기**: 952곡, 24개 컬럼
- **주요 컬럼**: `streams`, `bpm`, `danceability_%`, `energy_%`, `valence_%`, `acousticness_%` 등

---

## 🔍 분석 내용

1. **데이터 전처리** — 결측치 확인, `streams` 컬럼 타입 변환 (object → int64)
2. **Top 10 아티스트** — 스트리밍 합계 기준 인기 아티스트 집계 & 시각화
3. **오디오 피처 상관관계** — 7개 오디오 피처 간 상관관계 heatmap 분석
4. **분포 분석** — BPM / Streams 분포 시각화, 이상치 탐색

---

## 💡 주요 발견

- **스트리밍 분포**: 상위 1% 곡이 전체 스트리밍을 지배하는 롱테일 분포
- **인기 BPM**: 100~130 BPM 사이 곡들이 가장 많음 (정규분포)
- **오디오 피처 관계**:
  - `energy` ↔ `acousticness` = **-0.58** → 에너지 넘치는 곡일수록 어쿠스틱하지 않음
  - `danceability` ↔ `valence` = **0.41** → 신나는 곡일수록 긍정적인 감정도가 높음

---

## 🛠 환경

| 항목 | 버전 |
|------|------|
| Python | 3.12.7 |
| Jupyter Notebook | 7.2.2 |
| pandas | 2.2.2 |
| numpy | 1.26.4 |
| matplotlib | - |
| seaborn | 0.13.2 |

---

## 🚀 실행 방법

```bash
# 1. 레포 클론
git clone https://github.com/okzzinkyo/spotify-eda.git
cd spotify-eda

# 2. Jupyter Notebook 실행
jupyter notebook spotify_eda.ipynb
```

> **Note**: Kaggle에서 데이터셋을 직접 다운받아 같은 폴더에 넣어주세요.  
> CSV 로드 시 `encoding='latin-1'` 옵션 필요합니다.

---

## 📁 파일 구조

```
spotify-eda/
├── spotify_eda.ipynb   # 메인 분석 노트북
└── README.md
```
