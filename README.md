# 키즈노트

> 어린이집/유치원 알림장 서비스입니다.

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=Vite&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=black)

## 📖 프로젝트 소개
부모님과 선생님이 아이의 하루를 기록하고 소통할 수 있는 **모바일 웹 기반의 키즈노트**입니다.
기존 강의의 '감정 일기장' 로직을 활용하여, 아이의 기분 상태와 활동 내용을 날짜별로 기록하고 관리할 수 있도록 커스터마이징했습니다.

---

## 주요 기능

1.  **알림장(일기) 쓰기**: 아이의 기분(이모티콘), 오늘의 활동 내용, 날짜를 선택하여 작성할 수 있습니다.
2.  **월별 리스트 조회**: 메인 화면에서 월(Month)별로 작성된 알림장을 필터링하여 볼 수 있습니다.
3.  **정렬 기능**: 최신순, 오래된 순으로 알림장을 정렬하여 확인할 수 있습니다.
4.  **수정 및 삭제**: 작성한 알림장의 내용을 수정하거나 삭제할 수 있습니다.
5.  **로컬 데이터 저장**: `localStorage`를 활용하여 새로고침 해도 데이터가 유지되도록 구현했습니다.

---

## 🛠 기술 스택 (Tech Stack)

* **Frontend**: React.js, Vite
* **Routing**: React Router DOM (v6)
* **State Management**: React Context API, useReducer
* **Styling**: CSS (Module)
* **Deployment**: Vercel 

---

## 📂 폴더 구조 (Folder Structure)

```text
📦 src
 ├── 📂 components    # 재사용 가능한 UI 컴포넌트
 │    ├── Button.jsx         # 공통 버튼 (긍정, 부정, 기본)
 │    ├── Header.jsx         # 페이지 상단 헤더 (날짜 표시, 네비게이션)
 │    ├── Editor.jsx         # 알림장 작성 및 수정 폼
 │    ├── NoteItem.jsx       # 알림장 리스트의 개별 아이템
 │    ├── NoteList.jsx       # 알림장 리스트 및 정렬 필터
 │    └── EmotionItem.jsx    # 아이 기분 선택 이모티콘 컴포넌트
 │
 ├── 📂 pages         # 페이지 라우팅 단위
 │    ├── Home.jsx           # 메인 페이지 (월별 리스트)
 │    ├── New.jsx            # 새 알림장 작성 페이지
 │    ├── Edit.jsx           # 알림장 수정 페이지
 │    └── Note.jsx           # 알림장 상세 보기 페이지
 │
 ├── 📂 hooks         # 커스텀 훅
 │    └── useNote.jsx        # 알림장 데이터 CRUD 로직 (useDiary 응용)
 │
 ├── 📂 util          # 유틸리티 함수 및 상수
 │    ├── date.js            # 날짜 변환 및 포맷팅 함수
 │    ├── emotion.js         # 기분 아이콘 이미지 및 ID 관리
 │    └── constants.js       # 공통 상수 관리
 │
 ├── App.jsx          # 라우팅 설정 및 Context Provider
 └── main.jsx         # Entry Point
```

  1. **레포지토리 클론**
   ```bash
   git clone [https://github.com/사용자명/프로젝트명.git](https://github.com/사용자명/프로젝트명.git)
   cd 프로젝트명
   ```

   ```bash
  npm install
  # 또는
  yarn install
  ```

 ```bash
npm run dev
 ```

## 💡 트러블 슈팅 & 배운 점
 Context API 최적화: Provider를 분리하여 불필요한 리렌더링을 방지하는 방법을 학습했습니다.

날짜 처리: JavaScript Date 객체를 다루면서 월별 필터링 로직을 구현하는 데 어려움이 있었으나, new Date()의 특성을 이해하고 해결했습니다.

LocalStorage 동기화: useEffect를 사용하여 상태가 변경될 때마다 로컬 스토리지에 데이터를 저장하는 로직을 구현했습니다.


