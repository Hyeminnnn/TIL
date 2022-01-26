# TIL(Today I learned)

 #  python

## 1.개요

![파이썬 로고입니다.](https://www.python.org/static/img/python-logo@2x.png)



파이썬(Python)은 1990년 암스테르담의 귀도 반 로섬(Guide van Rossum)이 개발한 인터프리티 언어이다. 귀도는 파이썬이라는 이름을 자신이 좋아하는 코미디 쇼인 "몬티 파이썬의 날아다니는 서커스"에서 따왔다고 한다.

> 인터프리티 언어란 한 줄씩 소스 코드를 해석해서 그때그때 실행해 결과를 바로 확인할 수 있는 언어이다.



## 2.특징

1. 파이썬은 인간다운 언어이다. 아래 코드는 쉽게 해석된다.

```
if 4 in [1,2,3,4]: print("4가 있습니다.")
```

만약 4가 1,2,3,4 중에 있으면 "4가 있습니다."를 출력한다.라고 말이다. 

2.  파이썬은 간결하다.

   ```python
   # simple.py
   languages = ['python','perl','c','java']
   
   for lang in languages:
   	if lang in ['python','perl']:
   		print('%6s need interpreter' % lang)
   	elif lang in ['c', 'java']:
   		print('%6s need compiler' % lang)
   	else:
   		print('should not reach here.')
   ```

   3. 공식문서가 자세히 제공된다.

      [github 공식문서](https://github.com/)



# 적용해보기

## 22.01.25



> 오늘은 markdown을 이용해서 다양한 것들을 배워보았다.
>
> `백틱`이  꽤 중요한 기능을 한다.



이제 순서 있는 목록을 만들어보자.

* git bash 정리(*+space 바를 누르면 동그라미가 생성)
  * .start: 현재 경로 어딘지
  * ls : 파일이 뭐가 있는지
  * ls -a : 숨겨진 파일까지 보기 위해
  * touch: 파일 새로 생성
  * mkdir: 폴더 새로 생성
  * rm가 매우 중요하며 주의해야 함
    * 홈폴더에서 **rm -rf**를 사용할땐 매우 <span style="color:red">주의</span>가 필요
    * rm a.txt를 할때도 현재 경로 어딘지 확인



그럼 글씨체를 다르게 만들어 보는건?

*이탤릭체*

**보드체**

~~취소선~~

이렇게 가능하다 **참 쉽죠**?



## 22.01.26

### vscode로 GUI,CLI 환경 동시에 보기 , GIT 사용 



* GIT 명령어 정리

  1. git init : 현재 폴더를 깃이 관리하는 폴더로 만들자 

     -홈 폴더에 기입하지 않기 중요

     최초 1번만 기입

     터미널에 <span style="color:blue">(master)</span> 가 떠야 제대로 된 것 

     ```bash
     $ git init
     Initialized empty Git repository in ~ 
     ```
     
   2. git status : 현재 상황이 어떤지 보고싶을 때

              ```bash
              $ git status
              On branch master
              
              No commits yet
              
              nothing to commit (create/copy files and use "git add" to track)
              ```

​           -수시로 확인해줘서 현재 어떻게 진행 중인지 check!

   3. git add a.txt : woriking directory에 있는 파일을 staging area에 올리는 작업 
      
      -Untracked, Modified → Staged
      
      -한번 cycle을 돌리고 난 이후에는 `ctrl` + `s` (저장)해주고 **git add .** 만 해주면 자동 추가 
      
      ```bash
      # 특정 파일
      $ git add a.txt
      
      # 특정 폴더
      $ git add my_folder/
      
      # 현재 디렉토리에 속한 파일/폴더 전부
      $ git add .

​     

4. git commit -m '메시지' : 찰칵 후 저장소 

   -`'메시지'`는 아무거나 해도 상관은 없지만 본인이 잘 알아 볼 수 있도록 현재 변경사항들을 특징 할 수 있는 말로 할 것.

   ```bash
   $ git commit -m "first commit"
   [master (root-commit) c02659f] first commit 
   1 file changed, 0 insertions(+), 0 deletions(-)
    create mode 100644 a.txt # 이문구가 떠야 추가 되었다는 것을 알 수 있음 
   ```

   

5. git log :버전 확인하기

   -**git log --oneline** : 해쉬 값을 한 줄로 표현 해주는 명령어

   조금 있다 쓰일 checkout에서 확인 가능

   -커밋한 내용들을 확인 할 수 있음(ID,작성자,시간,메시지)



6. git checkout 해쉬값(7자리)

 ```bash
 $ git checkout 24e57dd
 Note: switching to '24e57dd'.
 ....
 HEAD is now at 24e57dd third commit
 ```





7. git checkout master : 처음으로 돌아가기



8. 여기서 git과 git hub 브릿지 이어주기 

   -git remote add origin 주소(본인)

   -git remote -v 

        ```bash
        $ git remote -v
        origin  https://github.com/Hyeminnnn/repo-test.git (fetch)
        origin  https://github.com/Hyeminnnn/repo-test.git (push)  #위아래 동일 주소로 뜨면 연결 성공
        ```

9. git push origin master :git hub에 올리기 

   

* 저장하기 -> git add . -> git commit -m '~~~~' -> git status -> git log --oneline : one cycle

  