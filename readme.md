# 팀원 소개 페이지

Git 커밋 협업을 통한 팀원 소개 페이지 프로젝트입니다.

## 프로젝트 구조

```
ryankor.github.io/
├── index.html          # 팀원 목록 페이지
├── member.html         # 개별 팀원 상세 페이지
├── members/           # 팀원 정보 JSON 파일 디렉토리
│   ├── members.json   # 팀원 목록 파일
│   └── example.json   # 예시 팀원 정보
└── image/             # 이미지 파일 디렉토리
```

## Git 협업 가이드

### 1. 저장소 클론 및 브랜치 생성

```bash
# 저장소 클론
git clone <repository-url>
cd ryankor.github.io

# 새 브랜치 생성 (본인의 이름 또는 아이디로)
git checkout -b add-member-<your-name>
```

### 2. 본인의 팀원 정보 추가

1. `members/` 디렉토리에 본인의 JSON 파일을 생성합니다.
   - 파일명: `본인아이디.json` (예: `honggildong.json`)

2. `members/example.json` 파일을 참고하여 본인의 정보를 작성합니다.

```json
{
  "id": "your-id",
  "name": "홍길동",
  "subName": "풀스택 개발자",
  "profileImage": "image/your-profile.png",
  "introduction": {
    "quote": "자기소개 한 줄",
    "detail": "자기소개 상세 내용"
  },
  "info": {
    "description": "간단한 소개",
    "birthday": "2000.01.01",
    "location": "서울시 강남구",
    "email": "your.email@example.com",
    "phone": "010-1234-5678"
  },
  "strengths": ["의사소통", "도전 정신", "리더십"],
  "skills": [
    { "name": "HTML", "progress": 10 },
    { "name": "CSS", "progress": 10 },
    { "name": "JavaScript", "progress": 15 }
  ],
  "licenses": ["정보처리기사"],
  "education": [
    {
      "name": "스파르타 대학교",
      "period": "2016.03.02 ~ 2020.02.20",
      "gpa": "4.0",
      "location": "서울시 강남구"
    }
  ],
  "experience": [
    {
      "period": "6개월",
      "company": "회사명",
      "term": "2023.01~2023.06",
      "team": "개발팀, 개발자",
      "task": "주요 업무",
      "project": {
        "name": "프로젝트명",
        "term": "2023.02~2023.05",
        "detail": "프로젝트 상세 설명"
      }
    }
  ],
  "projects": [
    {
      "title": "프로젝트명",
      "description": "프로젝트 설명",
      "image": "image/project-image.png",
      "link": "project.html"
    }
  ]
}
```

3. `members/members.json` 파일에 본인의 JSON 파일명을 추가합니다.

```json
{
  "members": [
    "example.json",
    "your-id.json"
  ]
}
```

4. 프로필 이미지를 `image/` 디렉토리에 추가합니다 (선택사항).

### 3. 변경사항 커밋 및 푸시

```bash
# 변경사항 확인
git status

# 변경사항 스테이징
git add members/your-id.json
git add members/members.json
git add image/your-profile.png  # 이미지가 있는 경우

# 커밋
git commit -m "Add: 홍길동 팀원 정보 추가"

# 푸시
git push origin add-member-<your-name>
```

### 4. Pull Request 생성

1. GitHub에서 Pull Request를 생성합니다.
2. PR 제목: `Add: [본인 이름] 팀원 정보 추가`
3. PR 설명에 본인의 간단한 소개를 작성합니다.

### 5. 코드 리뷰 및 머지

- 다른 팀원들의 코드 리뷰를 받습니다.
- 승인 후 메인 브랜치에 머지됩니다.

## 주의사항

1. **파일명 규칙**: JSON 파일명은 `본인아이디.json` 형식으로 작성하세요.
2. **JSON 형식**: JSON 파일의 문법 오류가 없도록 주의하세요.
3. **이미지 경로**: 이미지 파일은 `image/` 디렉토리에 저장하고, 경로는 `image/파일명.png` 형식으로 작성하세요.
4. **커밋 메시지**: 명확하고 간결한 커밋 메시지를 작성하세요.
5. **충돌 해결**: 다른 팀원과 동시에 수정한 경우 충돌을 해결해야 합니다.

## 예시

### 팀원 정보 추가 예시

```bash
# 1. 브랜치 생성
git checkout -b add-member-kim

# 2. JSON 파일 생성
# members/kim.json 파일 생성 및 작성

# 3. members.json 업데이트
# members/members.json에 "kim.json" 추가

# 4. 커밋 및 푸시
git add members/kim.json members/members.json
git commit -m "Add: 김철수 팀원 정보 추가"
git push origin add-member-kim
```

## 문의

프로젝트 관련 문의사항이 있으면 이슈를 생성해주세요.

---
Copyright ⓒ TeamSparta All rights reserved.
