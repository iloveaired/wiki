### GitHub 사용하기
 * [GitHub Page란 무엇인가?](https://help.github.com/categories/20/articles)


### 자바이야기1
 *http://goo.gl/FymS1a


### 추천자바 자료
* http://opentutorials.org/module/516
* http://www.jabook.com
* https://wikidocs.net/book/31
* http://www.vogella.com/tutorials/java.html  (중급)
* http://docs.oracle.com/javase
* http://docs.oracle.com/javase/tutorial/reallybigindex.html
* http://cafe.naver.com/prvd

### git 자료
* [git 게임으로 따라하기](http://learnbranch.urigit.com/)
* [Pro Git 설명](http://mobicon.tistory.com/182)
* [git 기초 쿨 해외 블로그](http://rogerdudler.github.io/git-guide/index.ko.html)
* [svn git 비교](http://www.slideshare.net/einsub/svn-git-17386752)
#### git 명령어
> * git checkout -b step-2  <--  branch, checkout 동시에
* git branch <-- branch 리스트 보기

* 38 page : git commit -a  <- 모든 변경된 파일 commit
* commit된 후에 변경된 파일 변경후 다시 commit 된 상태파일 가져오기(다시 원복)
> git checkout app/index.html


* Create a new repository on the command line
```
touch README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/iloveaired/okandroid.git
git push -u origin master
```

* Push an existing repository from the command line 
```
git remote add origin https://github.com/iloveaired/okandroid.git
git push -u origin master
```