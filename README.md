#SK PLAN-IT(Soccer Kick Plan, get It)#
##PROJECT PERIOD : 16.02.16 ~ 16.04.01##
=====

## [SK PLAN-IT][1] 이란?
SK PLAN-IT은 한마디로 축구 동호회 사이트이다. 기존 카페나 블로그형식으로 이루어져있는 동호회는 내주변 동호회를 한눈에 확인 할수 없다는 단점을 지도 daum api를 활용하여 사용자에게 편리하게 주변을 확인하고 가입할 수 있도록 하였다. 또한 축구 동호회인 만큼 동호회 생성, 커뮤니티 게시판, 축구 전략을 짜고 공유할 수 있는 공간, 그리고 갤러리등 다양한 서비스를 제공한다.



## 사용기술 ##
***FRONT END 와 BACK END의 분리된 개발***

***FRONT END***
```
  -- FRONT END
    : BOWER를 통한 라이브러리 관리(bower.json bower-installer).
    : Javascript, JQuery, CSS, Bootstrap3, HTML5, Ajax.
    : SPA(Single Page Application)형태를 나타내기 위한 Ajax방식으로만
      프로젝트 구성후 하이브리드앱 제작.
  
  bower.json
  "dependencies": {
		"bootstrap": "~3.3.4",
		"jquery": "2.0.3",
		"jquery-ui": "1.10.4",
		"blueimp-file-upload": "jquery-file-upload#^9.11.2",
		"font-awesome" : "https://github.com/tdg5/font-awesome-bower.git/#v4.3.0",
		"jquery-smooth-scroll" : "https://github.com/kswedberg/jquery-smooth-scroll.git",
		"jquery-throttle-debounce" : "https://github.com/cowboy/jquery-throttle-debounce.git",
		"interact" : "https://github.com/taye/interact.js.git",
		"html2canvas" : "https://github.com/niklasvh/html2canvas.git",
		"jscolor" : "https://github.com/EastDesire/jscolor.git",
		"flexslider" : "https://github.com/woothemes/FlexSlider.git",
		"masonry" : "4.0.0",
		"imagesloaded" : "https://github.com/desandro/imagesloaded.git",
		"handlebars" : "https://cdnjs.cloudflare.com/ajax/libs/handlebars.js/3.0.1/handlebars.js"
	},
	"install": {
		"path": "src/main/webapp/lib",
		"sources": {
			"bootstrap": "bower_components/bootstrap/dist/**",
      		"jquery": "bower_components/jquery/**",
      		"blueimp-file-upload": "bower_components/blueimp-file-upload/**",
      		"font-awesome": "bower_components/font-awesome/**",
      		"jquery-smooth-scroll" : "bower_components/jquery-smooth-scroll/jquery.smooth-scroll.js",
      		"jquery-throttle-debounce" : "bower_components/jquery-throttle-debounce/jquery.ba-throttle-debounce.min.js",
      		"interact" : "bower_components/interact/dist/interact.js",
      		"html2canvas" : "bower_components/html2canvas/build/html2canvas.js",
      		"jscolor" : "bower_components/jscolor/jscolor.js",
      		"flexslider" : "bower_components/flexslider/**",
      		"masonry" : "bower_components/masonry/dist/**",
      		"imagesloaded" : "bower_components/imagesloaded/imagesloaded.pkgd.min.js",
      		"handlebars" : "bower_components/handlebars/index.js"
		}
	}
```



***BACK END***
```
  -- BACK END
    : Gradle을 통한 Build관리.
    : Spring Framework(Only Rest방식으로 JSON DATA return),
    : Mysql DB, Mybatis, eXERD, Node JS(socket.io, express, mysql).
    
  build.gradle
  apply plugin: 'eclipse-wtp' // 이클립스 관련 설정파일 생성/삭제
  apply plugin: 'war'
  apply plugin: 'java'
  
  compileJava {
  	options.encoding = "UTF-8"
  	sourceCompatibility = 1.8
  }
  
  eclipse {
  	wtp {
  		facet {
  			facet name: 'jst.web', version: '3.1'
        		facet name: 'jst.java', version: '1.8'
      	}
    	}
  }
  
  repositories {
  	mavenCentral() 
  }
  
  dependencies {
  	compile 'mysql:mysql-connector-java:5.1.37'
  	compile 'org.mybatis:mybatis:3.3.0'
  	compile 'org.mybatis:mybatis-spring:1.2.3'
  	compile 'org.springframework:spring-webmvc:4.2.3.RELEASE'
  	compile 'org.springframework:spring-jdbc:4.2.3.RELEASE'
  	compile 'org.springframework:spring-test:4.2.3.RELEASE'
  	compile 'commons-dbcp:commons-dbcp:1.4'
  	compile 'jstl:jstl:1.2'
  	compile 'commons-fileupload:commons-fileupload:1.3.1'
  	compile 'net.coobird:thumbnailator:0.4.8'
  	compile 'org.imgscalr:imgscalr-lib:4.2'
  	compile 'org.reflections:reflections:0.9.10'
  	compile 'log4j:log4j:1.2.17'
  	compile 'com.fasterxml.jackson.core:jackson-databind:2.6.4'
  	compile 'org.aspectj:aspectjweaver:1.8.7'
  	compile 'junit:junit:4.12'
  	compile 'org.slf4j:slf4j-api:1.6.6'
  	
  	providedCompile 'javax.servlet:javax.servlet-api:3.1.0'
  }
```


## 팀원 ##
주철민(팀장), 김대오, 최승완, 조영일

## [Demo & Detail][2] ##
[1]:https://github.com/java77-final-project/web-project/
[2]:http://blog.naver.com/iamcyi
