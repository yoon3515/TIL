# 22.12.26(월)
> Git 입문 : 파일/폴더 생성부터 repository에 커밋 저장
## 파일/폴더 생성과 삭제
1. 폴더 생성 : mkdir
    ```bash
        mkdir folder1 folder2 'folder 3'
    ```

   - *띄어쓰기* 로 한 번에 여러개의 폴더 생성 가능
   - 폴더명에 공백을 주고싶을 땐 폴더명을 (' ')로 묶어주기

2. 파일 생성 : touch
    ```bash
    touch a.txt
    ```
   - *띄어쓰기*로 한 번에 여러개의 파일 생성 가능 
   - 파일명 앞에 . 를 써서 *숨김파일* 만들 수 있다. 

3. ls : list segments
    - 현재 작업중인 디렉토리의 폴더/파일 목록을 보여줌
    - a : all 옵션. 숨김파일까지 모두 보여줌 
    - l : long 옵션. 파일정보(용량, 수정날짜 등) 보여줌
    ```bash
    ls
    ls -a
    ls -l
    ls -a-l #옵션 함께 적용
    ls -al  #옵션 축약 기능
    ```

4. mv (move)
   ```bash
   mv a.txt folder # 파일 a를 folder라는 폴더에 넣을 때
   mv a.txt b.txt # 파일 a 이름을 b로 바꿀 때 
   ```
   - 파일을 폴더로 이동시킬 때 사용
   - 폴더/파일 이름 변경
   - 파일 이동시킬 때 이동시킬 폴더가 꼭 존재해야 함

5. 