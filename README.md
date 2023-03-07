# Git Convention 👋

### 목차
1) [Git Naming Convention 📫](#git-naming-convention)
2) [Git Readme Convention 📄](#git-readme-convention)
3) [Git Commit Convention 💬](#git-commit-convention)


<br/>

# Git Naming Convention
<br/>

- 특수문자, CamelCase 금지  
- 소문자 사용  
- 대시 사용  
- 명확하게 작성  
- 일관성있게 작성  
- '프로젝트 이름-개발 환경-프로젝트 목적' 형태로 구성  

#### dreamers 프로젝트
```
dreamers-php-frontend,backend
```

<br/>


## Git Readme Convention
<br/>

1) **프로젝트명**  
<br/>

2) **프로젝트 설명**
- 애플리케이션이 무엇을 하는지,
- 왜 그 기술을 사용했는지,
- 여러분이 당면했던 문제나 나중에 추가하고 싶은 기능이 무엇인지
<br/>

3) **목차 (선택)**
<br/>

4) **프로젝트 설치 및 실행 방법**  
- 프로젝트를 설치할 수 있는 방법과 필요한 경우 dependencies를 포함해 작성해야 합니다.
- 개발 환경을 세팅하고 실행할 수 있는 단계적인 설명을 제공하세요.
<br/>

5) **프로젝트 사용 방법**  
- 사용자/기여자들이 프로젝트를 이용할 수 있는 방법과 예시
- 프로젝트 실행 예시 화면의 스크린샷, 구조나 디자인 원칙
<br/>

6) **팀원 및 참고 자료**  
- 팀이나 조직 단위로 작업한 프로젝트라면 팀원들의 깃허브 프로필과 SNS 링크도 연결
- 튜토리얼이나 자료를 참고했다면 링크도 같이 첨부  
<br/>

7) **라이센스**  
```
# Apache License
아파치 재단에서 자체 소프트웨어에 적용하기 위한 라이선스다. 개인적/상업적 이용, 배포, 수정, 특허 신청이 가능하다.

# MIT License
MIT 학생들을 위해 개발한 라이선스이며 개인 소스에 이 라이선스를 사용하고 있음을 표시만 해주면 된다.  
무료로 사용할 오픈소스에서 가장 많이 확인할 수 있는 라이선스다.

# BSD License
버클리 캘리포니아대학에서 개발한 라이선스로 MIT와 동일하게 표시만 지켜주면 된다.

# Beerware
오픈소스 개발자에게 맥주를 사줘야 하는 라이선스다.
```
<br/>

**+++ (선택)**

8) **뱃지**  
- 뱃지를 사용하면 중요한 툴로 연결해 주거나 포크, 기여자, 오픈된 이슈 등 여러분의 프로젝트와 관련된 간단한 통계를 보여줄 수도 있다.
-  shields.io
<br/>

9) **기여 가이드라인**  
- 향후 충돌을 막기 위해서 오픈소스 프로젝트에 사용되는 라이센스가 올바른 것인지 확인
- https://www.contributor-covenant.org/
- https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/setting-guidelines-for-repository-contributors  
<br/>

10) **테스트**
- 애플리케이션의 테스트를 위해 예제 코드와 실행 방식  
<br/>

#### 참고   
Readme 자동화 도구
- https://rahuldkjain.github.io/gh-profile-readme-generator/
- https://github.com/kefranabg/readme-md-generator


<br/>


# Git Commit Convention
<br/>

### 메세지 구조 
먼저 커밋 메시지는 크게 제목, 본문, 꼬리말 세 가지 파트로 나누고, 각 파트는 빈줄을 두어서 구분합니다.

```
type(옵션): [#issueNumber - ]Subject  // -> 제목  
(한 줄을 띄워 분리합니다.)   
body(옵션) //  -> 본문   
(한 줄을 띄워 분리합니다.)   
footer(옵션) // -> 꼬리말  
``` 
- type : 어떤 의도로 커밋했는지를 type에 명시
- subject : 최대 50글자가 넘지 않도록 하고 마침표는 찍지 않습니다. 영문으로 표기하는 경우 동사(원형)를 가장 앞에 두고 첫 글자는 대문자로 표기
- body : 긴 설명이 필요한 경우에 작성. 무엇을 왜 했는지를 작성. 최대 75자를 넘기지 않도록 합니다.   
- footer : issue tracker ID를 명시하고 싶은 경우에 작성

<br/>

### 타입

**[ 태그: 제목 ]**

| 태그이름 | 설명 | 태그의 종류
|:---|:---:|:---:| 
|Feat|새로운 기능을 추가할 경우|기능|
|Fix|버그를 고친 경우|기능|
|Design|CSS 등 사용자 UI 디자인 변경|기능|
|File| 이미지 등 파일 추가
|!BREAKING CHANGE|커다란 API 변경의 경우|기능|
|!HOTFIX|급하게 치명적인 버그를 고쳐야하는 경우|기능|
|Style|코드 포맷 변경, 세미 콜론 누락, 코드 수정이 없는 경우|개선|
|Refactor|프로덕션 코드 리팩토링|개선|
|Comment|필요한 주석 추가 및 변경|개선|
|Docs|문서를 수정한 경우| 
|Test|테스트 추가, 테스트 리팩토링(프로덕션 코드 변경 X)| 
|Chore|빌드 태스트 업데이트, 패키지 매니저를 설정하는 경우(프로덕션 코드 변경 X)| 
|Rename|파일 혹은 폴더명을 수정하거나 옮기는 작업만인 경우| 
|Remove|파일을 삭제하는 작업만 수행한 경우| 



#### 제목  
> 제목의 처음은 동사 원형으로 시작합니다.   
> 총 글자 수는 50자 이내로 작성합니다.   
> 마지막에 특수문자는 삽입하지 않습니다. 예) 마침표(.), 느낌표(!), 물음표(?)   
> 제목은 개조식 구문으로 작성합니다.
 
1) 만약 영어로 작성하는 경우 다음의 규칙을 따릅니다.  
> 첫 글자는 대문자로 작성합니다.  
> "Fix", "Add", "Change"의 명령어로 시작합니다.

2) 한글로 제목을 작성하는 경우 다음의 규칙을 따릅니다.  
> "고침", "추가", "변경"의 명령어로 시작합니다.
 
<br/>

### 본문   
> 본문은 한 줄 당 72자 내로 작성합니다.  
> 본문 내용은 양에 구애받지 않고 최대한 상세히 작성합니다.  
> 본문 내용은 어떻게 변경했는지 보다 무엇을 변경했는지 또는 왜 변경했는지를 설명합니다.

<br/>

### 꼬리말   
> 꼬리말은 optional이고 이슈 트래커 ID를 작성합니다.  
> 꼬리말은 "유형: #이슈 번호" 형식으로 사용합니다.  
> 여러 개의 이슈 번호를 적을 때는 쉼표로 구분합니다.  
> 이슈 트래커 유형은 다음 중 하나를 사용합니다.
>   - Fixes: 이슈 수정중 (아직 해결되지 않은 경우)
>   - Resolves: 이슈를 해결했을 때 사용  
>   - Ref: 참고할 이슈가 있을 때 사용  
>   - Related to: 해당 커밋에 관련된 이슈번호 (아직 해결되지 않은 경우)  
>   ex) Fixes: #45 Related to: #34, #23


### Git Commit 예제
```
Feat: "추가 로그인 함수"   

로그인 API 개발   

Resolves: #123   
Ref: #456   
Related to: #48, #45
```

