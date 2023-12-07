--------------------------------------------------
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
</code>
</pre>

------------------------------------------

# ⚙지역과 원격 저장소 브랜치 연동
<pre><code>
#원격 저장소 복제 연동
$ git clone https://github.com/ai7dnn/repo-sync.git

#원격 저장소 수정 사항 pull로 지역 저장소로 가져오기
$ git pull origin main
$ git pull

#원격 저장소 수정 사항 fetch로 지역 저장소로 가져와 병합하기
$ git fetch origin main
$ git fetch
$ git merge origin/main

#지역 저장소 수정 사항 push로 원격 저장소 보내기
$ git push origin main
$ git push
</code>
</pre>
------------------------------------------

# 🔒임시저장 stash
<pre><code>
#작업 디렉토리와 스테이징 영역을 숨김(stash)에 저장하고 작업 폴더를 정리
$ git stash
$ git stash –m ‘메시지’
$ git stash save
$ git stash save ‘메시지’

#최근 또는 지정된 임시 저장소 내용을 가져와 반영하고 삭제
$ git stash pop
$ git stash pop stash@{n}

#최근 또는 지정된 임시 저장소 내용을 가져와 반영, 작업 디렉토리에 반영, stash 목록은 그대로
$ git stash apply
$ git stash apply stash@{n}
  
#최근 또는 지정된 임시저장소 내용을 가져와 반영, 작업 디렉토리와 스테이징 영역도 반영, stash 목록은 그대로
$ git stash apply --index
$ git stash apply --index stash@{n}
</code>
</pre>
------------------------------------------

# 다양한 브랜치 병합
<pre><code>
#기준 브랜치에서 hotfix 브랜치 병합
$ git merge hotfix
  • fast-forward, 3-way merge
  
#무조건 3-way 병합 수행
$ git merge --no-ff hotfix
  
#fast-forward인 경우에만 병합 진행
$ git merge --ff-only hotfix
  
#현재 브랜치에서 커밋 하나만 생성해서 병합
$ git merge --squash hotfix
</code>
</pre>
------------------------------------------
