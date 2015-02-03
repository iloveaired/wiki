### [안드로이드 이야기 #1 1](http://goo.gl/VUe7H9)
> * http://bit.ly/afreeca201402
* https://github.com/kenu/okandroid
* http://www.memoriesreloaded.net/2014/01/blog-post_30.html
* 개발도구 인코딩 utf-8
   * eclipse.ini 마지막줄에 -Dfile.encoding=utf-8
*  SDK Manager
	* 개발플랫폼 다운로드 :  4.3기준(2014.06)
* AVD 만들기
   1. AVD manager 실행
   2. new 버튼 클릭
   3. Target 항목 : Android 4.3 API 18
   4. Device : Galaxy Nexus 4.65 inch 720*1280 xhdpi
   5. 윈도우일결우 Memory 768M 이하로 조정
   6. avd이름 avd18  api버젼으로하는게 유리
   7. avd 선택후 start
   8. 5분정도 기다려야 부팅됨..느림
 
 * 추천 서적
 	* Do it 안드로이드 
 	* 나홀로 개발자를 위한 안드로이드 프로그래밍의 모든것(www.godev.kr)
 	
### [안드로이드 이야기 #1 2](http://goo.gl/eu6Juu)

> * 안드로이드 프로젝트 만들기
 1. java 퍼스펙티브
 2. file->new-> android application project 선택
* 안드로이드 파일구조  find . -type d

```
aired@LEE_YOUNG_KWAN /c/dev/android/workspace/HelloAndroid
$ find . -type d
.
./.settings <- 이클립스 설정정보
./assets    <- 로컬 자원(이미지,html)
./bin       <- 클래스 자동 생성 폴더  
./gen       <- apk 만들어지는곳 
./libs      <- jar 파일 위치
./res       <- 리소스(인덱싱됨, R.java와 연관)    
./res/drawable-hdpi <- 이미지(소문자, 0-9...)
./res/drawable-ldpi
./res/drawable-mdpi
./res/drawable-xhdpi
./res/layout <- xml ui파일(view 역할)
./res/menu
./res/values <- string (문자열,다국어, 기기별)
./src        <- 자바코드
```
 * 강의 정리 : http://bit.ly/af-android

### [안드로이드 이야기 #2 1](http://goo.gl/bqi9Jp)
 * 키워드
> * polyglot
* http://jscon.ebrainus.com/
* http://firejune.com/



### [안드로이드 이야기 #2 2](http://goo.gl/372mxG)
> * balasmiq : mockup 툴
45분까지...








### [node js로 놀기 & GitHub 시작하기](http://goo.gl/bEQa3K)
```
* nodejs.org 에서 다운로드
* 
```
  * 다큐먼트 http://bit.ly/afreeca201312
  * http://nodeqa.com/
  * https://github.com/joyent/node/wiki
  * 초보 시작점 : http://www.nodebeginner.org/index-kr.html

### [node js로 놀기 & GitHub 시작하기2](http://goo.gl/hkd9C0)
  * 35분 ~  : iloveaired.github.io/  페이지 만들기 예제 (쿨)

### [node js로 놀기 socket io, node debugging 1](http://goo.gl/cXTmVa)
> 웹소켓 관련 : 30분 http://m.mkexdev.net/98
  http://www.nodebeginner.org/index-kr.html
  
### [node js로 놀기 socket io, node debugging 2](http://goo.gl/bg3vvX)
> http://balsamiq.com/download/
node 디버깅 : http://edoli.tistory.com/60
### [node js로 놀기 socket io, node debugging 3](http://goo.gl/0R14l2)
>
** node 디버깅 : http://edoli.tistory.com/60