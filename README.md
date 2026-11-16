# IT 학습 기록

Excalidraw로 정리한 학습 내용을 읽기 쉬운 HTML로 보관하는 개인 학습 저장소입니다. 원본과 정리 문서를 함께 남기고, 내용을 검수한 뒤 GitHub에 반영합니다.

## 문서 보기

[index.html](index.html)을 다운로드한 저장소에서 브라우저로 열면 전체 분류를 탐색할 수 있습니다. 별도 설치나 빌드가 필요하지 않습니다. GitHub 파일 화면에서는 HTML 코드가 표시되므로, 렌더링된 문서는 로컬 브라우저에서 확인하세요.

현재는 기본 분류만 준비되어 있습니다. 학습 문서는 Excalidraw 자료를 전달하면 추가됩니다.

## 학습 분류

| 분류 | 폴더 | 다루는 내용 |
| --- | --- | --- |
| 컴퓨터 구조 | [computer-architecture](topics/computer-architecture/index.html) | CPU, 메모리, 명령어 |
| 운영체제 | [operating-systems](topics/operating-systems/index.html) | 프로세스, 스레드, 메모리 관리, 파일 시스템 |
| 네트워크 | [networks](topics/networks/index.html) | 통신 계층, 프로토콜, 네트워크 구조 |
| 데이터베이스 | [databases](topics/databases/index.html) | 모델링, SQL, 트랜잭션, 인덱스 |
| 자료구조 | [data-structures](topics/data-structures/index.html) | 배열, 리스트, 트리, 해시 등 |
| 알고리즘 | [algorithms](topics/algorithms/index.html) | 탐색, 정렬, 문제 해결, 복잡도 |
| 프로그래밍 언어 | [programming](topics/programming/index.html) | 문법, 실행 원리, 언어별 개념 |
| 소프트웨어 설계 | [software-design](topics/software-design/index.html) | 설계 원칙, 디자인 패턴, 아키텍처 |
| 웹 | [web](topics/web/index.html) | 브라우저, 프런트엔드, 백엔드 |
| 보안 | [security](topics/security/index.html) | 인증, 인가, 암호화, 취약점 |
| 클라우드·DevOps | [cloud-devops](topics/cloud-devops/index.html) | 인프라, 컨테이너, 배포, 운영 |
| AI·머신러닝 | [ai-ml](topics/ai-ml/index.html) | 모델, 학습 방법, AI 시스템 |

여러 분류에 걸친 자료는 핵심 주제에 맞춰 한 곳에 보관합니다. 필요한 경우 하위 분류를 추가합니다.

## 학습 자료 추가하기

1. 학습한 내용을 `.excalidraw` 파일로 정리합니다.
2. 에이전트에게 파일을 첨부하거나 로컬 경로를 전달하고 HTML 정리를 요청합니다.
3. 에이전트가 내용을 분석해 원본을 보관하고 적절한 분류에 HTML을 작성합니다.
4. 안내받은 HTML을 브라우저에서 열어 내용과 표현을 검수합니다.
5. 수정이 필요하면 요청합니다. 검수가 끝나면 커밋·푸시를 명시적으로 요청합니다.

요청 예시:

> `/path/to/process-thread.excalidraw`를 분석해서 학습 문서로 정리해줘.

검수 후 예시:

> 검수 완료했어. 이번 변경을 커밋하고 GitHub에 푸시해줘.

HTML을 작성하는 단계에서는 커밋하거나 푸시하지 않습니다. 최초 연결 시 사용할 GitHub 저장소 주소가 필요합니다. GitHub Pages를 통한 웹 공개는 별도 설정 작업입니다.

## 파일 구조와 이름

```text
study/
├── README.md
├── AGENTS.md                  # 에이전트의 반복 작업 절차
├── .gitignore
├── index.html                 # 전체 분류
├── assets/
│   └── style.css              # 공통 스타일
├── sources/
│   └── <category>/            # 변경 없이 보관한 Excalidraw 원본
└── topics/
    └── <category>/
        ├── index.html         # 분류별 학습 문서 목록
        └── <short-name>.html  # 자료가 추가되면 생성
```

문서 이름은 `process-thread.html`처럼 짧은 영문 소문자와 하이픈으로 구성합니다. 문서 제목과 본문은 한국어로 작성합니다. 대응하는 원본은 `sources/operating-systems/process-thread.excalidraw`처럼 동일한 기본 이름으로 보관합니다. HTML은 상대 경로를 사용하므로 저장소 폴더 전체를 함께 유지하세요.

원본에 없는 보충 설명은 구분해서 표시하고, 해석이 불명확한 부분은 검수 항목으로 안내합니다. 상세 작업 규칙은 [AGENTS.md](AGENTS.md)에 있습니다.
