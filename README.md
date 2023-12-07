# 📌Git bash 기본 명령어 모음

<pre><code>
# 깃 주요 6가지 설정
$ git config --global user.name minjeong0429         #사용자 이름
$ git config --global user.email mjmj328@naver.com   #사용자 전자메일
$ git config --global core.autocrlf true             #줄바꿈 자동변환
$ git config --global core.safecrlf false            #줄바꿈 안전 설정
$ git config --global core.editor 'code --wait'      #기본 편집기 설정
$ git config --global init.defaultBranch main        #기본 브랜치 이름

# 리눅스 명령어 1(폴더관련)
$ pwd           #print working directory
$ cd            #change directory
$ mkdir dname   #make directory
$ ls            #file or folder list

# 리눅스 명령어 2(파일관련)
$ touch fname      #빈파일 fname 생성
$ echo git bash
$ echo 'print()'   #출력
$ cat fname        #파일 내용 보이기
$ cp a b           #파일 a를 b로 복사
$ mv f1 f2         #파일 f1을 f2로 이름 수정

# 리눅스 명령어 3(삭제)
$ rm fname #파일 fname 삭제
$ rm -rf dname #하부에 서브폴더와 파일이 있어도 폴더 삭제

# 저장소 생성
$ git init basic  #저장소 생성
$ cd basic        #폴더 이동
$ ls -al          #파일 확인

</code
</pre>
