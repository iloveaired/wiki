### GitHub 사용하기
 * [GitHub Page란 무엇인가?](https://help.github.com/categories/20/articles)



### git 자료
* [git 게임으로 따라하기](http://learnbranch.urigit.com/)
* [Pro Git 설명](http://mobicon.tistory.com/182)
* [git 기초 쿨 해외 블로그](http://rogerdudler.github.io/git-guide/index.ko.html)
* [svn git 비교](http://www.slideshare.net/einsub/svn-git-17386752)
* [누구나 쉽게따라하는  ](https://backlogtool.com/git-guide/kr/intro/intro1_1.html)


### git 명령어
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

### TIP
 *  [.gitignore 자동생성](http://www.gitignore.io/cli)