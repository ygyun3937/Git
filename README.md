# Git 주의사항

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
