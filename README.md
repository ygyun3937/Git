# Git 관련 이것저것

## Configs
### local
: 해당 레포지토리(폴더)내에서만 아래 설정을 사용하겠다.
```bash
git config --local user.name "username"
git config --local user.email "yg@abc.com"
```

### global
: 전역 설정 ㅇㅋ?
```bash
git config --global user.name "username"
git config --global user.email "yg@abc.com"
```

## 특정파일 변경사항에 포함되지 않게 설정하기(커밋에 포함되지 않게 하기)
ex) 빌드파일 등등..

`.gitignore` 에 파일 확장자규칙이나 파일명, 폴더명을 명시하면 해당 소스는 변경사항에 포함되지 않는다.  


## Default branch 를 바꿨을때
ex) `main` -> `master`  
  
클론한 레포지토리 폴더 경로에서 아래 명령어로 브런치를 바꿔줘야 한다.  
이 과정 없이 커밋을 날리면 기존 `main`브런치에서 작업하는게 되버려  
커밋을 했을때 깃허브서버에 `main` 브런치가 하나 생성이 되어버리고 만다.  
```bash
git branch -m main master
git fetch origin
git branch -u origin/master master
git remote set-head origin -a
```

### Git 폴더 전체 업로드 방법
```bash
1. 업로드 폴더 상위로 이동
2. git bash 클릭 (우클릭 하면 Git Bash Here)
3. git remote add origin "업로드할 깃허브 repository 주소"
4. git status
5. git add .
6. git commit -m "커밋 메시지"
7. git remote -v
8. git push origin "branch 이름"
참고 링크 : https://vanillacreamdonut.tistory.com/193
```

### Git Error Message
: failed to push some refs to에 대한 해결방법
```bash
1. 업데이트 진행 (fetch)
git pull {원격저장소 별칭 보통은 origin} master
2. Push
결론 : 업데이트가 안된 상태로 Push 할려니 안되는거
참고 링크 : https://lala9663.tistory.com/10
```
