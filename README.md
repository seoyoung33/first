# HTML
## Hyper Text Markup Language
### HTML은 웹문서의 구조를 담당하는 언어이다.
* HTM에서 구조는 `<>`로 묶인 태그로 작성한다.
* `<시작태그></닫기태그>`
* `<빈태그>`
* 시작과 닫기태그는 한쌍의 요소로 불린다.
### HTML 구조태그
* HTML5 버전 선언하는 `<!doctype html>`
* HTML 웹브라우저 구조 처리하는 태그들
1. `<html></html>`
2. `<head></head>`
3. `<body></body>`
----
# git&gitHub
* 버전관리 프로그램 git
* 버전 파일, 폴더들을 저장하는 저장소 gitHub
## git 용어와 뜻
* 작업 디렉터리 : 실제 작업하는 로컬 저장소 (윈도우 탐색기 개념)
* 스테이징 : 깃허브에 작업 업로드 전 파일을 대기시키는 대기소
* repository : 대기소(stage)에 파일 대기 후 최종 gitHub 업로드 저장소
## 주의사항
* 당일 작업 시작 기준 gitHub 저장소와 로컬저장소의 파일, 폴더 상태가 같아야한다.
* 동일한 저장소를 관리하는 사람일 경우 작업 컴퓨터가 달라도 gitconfig에 등록된 이름, 이메일이 동일해야 한다.
----
# 주요 단축키 모음
* `Ctrl + /` 한줄 주석
* `Shift + Alt + A` 선택한 영역만 주석
----
# 처음 git을 이용한 gitHub 저장소 업로드 시 해야하는 순서
1. 현재 사용중 로컬 저장소를 git 저장소 등록 `git init`
2. 위 1번 정상 등록 시 경로에 (master) 표시출력
3. master -> main으로 최상위 경로명칭을 변경하기 위해 `git branch -m main` 작성
4. gitHub 저장소 생성 후 저장소 주소 복사
5. 현재 로컬 저장소 gitHub 저장소 연결 `git remote add origin 주소붙여넣기`
6. `git status` 현재 상태 확인 (스테이징, 작업디렉터리, 저장소)
7. 위 6번 결과 파일이 빨간색으로 출력될 경우 `git add 파일명` 스테이징 올리기
8. `git status` 위 7번에서 올린 파일이 초록색으로 변경된 것 확인 가능
9. `git commit -m '기록메세지'` 스테이징 파일을 저장소에 올리기 위한 기록설정
10. `git push origin main` 깃허브 저장소에 최종 파일, 폴더 업로드
11. 위 10번 처음 진행 시 깃허브 계정 인증 화면 나오니 인증 진행 후 저장소 F5
----
## 다른 환경에서 이어서 작업해야 하는 경우
1. 폴더 생성하기 -> vs code 폴더 연결
2. gitHub 저장소 주소 복사
3. vs code 돌아와서 ctrl + J 터미널 실행 후 Git bash 환경으로 변경
4. `git clone 저장소 주소붙여넣기`
5. 터미널 경로 오른쪽에 `main` 또는 `master` 표시가 있는지 확인
6. 위 5번에서 표시가 없다면 `cd 복제한폴더명`
7. 자유롭게 수정 후 파일 저장
8. 터미널에 `git status` 업로드 안된 파일 빨간색 색 확인
9. `git add 파일명` 수정한 파일 스테이지에 업로드하기
10. `git status` 위 9번 업로드 됐는지 확인 (초록색 변경)
11. `git commit -m '메세지'` 수정파일에 대한 기록 메세지 작성
12. `git push origin main` 깃허브 저장소에 업로드
## 태그와 속성, 값
* 속성 : 태그마다 여러 속성을 부여해야 할 경우
1. 미리 정의된 속성
2. 특별한 기능을 하는 속성
3. 시작 태그에만 사용됨
4. 순서, 갯수제한은 없음 (ex.제목 글자색="빨강" 글꼴="프리텐다드")
* 값 : 속성이 가지는 값
1. 큰따옴표("") 작은따옴표('')
2. 속성이 가진 고유 값
3. 개발자가 기본 규칙 내에서 지정할 수 있는 사용자 지정값 설정
### html의 속성과 값
* html lang="ko" -> 언어를 한국어로 지정하겠다
* 컴퓨터의 화면 낭독 소프트웨어 "스크린 리더" -> 시작장애인을 위한 설정
### meta의 속성과 값
* meta charset="UTF-8" -> 문자열을 유니코드로 다국어 지원을 하겠다
* 설정하지 않으면 글자가 깨지거나 오류가 생길 수 있으니 주의
* 설정값들은 Head에 저장됨
* <meta name="keywords"content=""> : 사용자가 쓰는 검색어(키워드)
* <meta name="description"content=""> : 검색 시 아래부분에 있는 내용. 요약설명