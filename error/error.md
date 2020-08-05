# error

## Git error CRLF will be replaced by LF or 반대 
맥,리눅스 개발자와 윈도우 개발자가 git으로 협업할때 발생하는 경우가 있다

```
// whitespace에러

warning: LF will be replaced by CRLF in getting-started/package-lock.json.
The file will have its original line endings in your working directory
```

윈도우 시스템에서는 줄(line)이 CR(Carriage Return)와 LF(Line Feed) CRLF로 이루어 져있는 반면에 유닉스 시스템에서의 줄(line)의 끝이 LF(Line Feed)로 이루어져 있다
이러한 다른점 때문에 혼란이 오는것이다

<strong>해결</strong>  
`core.autocrlf`를 사용하기!  
깃은 자동 변화기가 있으므로 윈도우 사용자의 경우 CRLF를 LF로 유닉스 사용자의 경우는 LF를 CRLF로 변환해준다

```
//해당 프로젝트만 적용하고 싶으면 
git config core.autocrlf true

//모두 적용하고 싶으면
git config --global core.autocrlf true

//단 반향만 원하면 input
git config --global core.autocrlf true input

//경고 메세지 알람 끄기 safecrlf = false
git config --global core.safecrlf false
```