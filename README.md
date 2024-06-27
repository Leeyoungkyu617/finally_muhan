![2](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/179dfb2d-6a35-4b79-8ad5-8266b5ae2448)![1](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/1a91db43-c284-4bed-a3c0-9a86f4cc5e8e)# Muhan 
## 주요 구현 기능  
[SpringMVC]     
[myBatis]  
[Ajax]  
[log4j]  

## 개발완료 시연 주요 화면
![Uploading 1![Uploading 2.png…]![15](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/63b39ca3-7b91-4bf1-a61a-2662a4d55844)
![14](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/e9a3f2df-974c-4e50-9bb2-cc2890fe2a7c)
![13](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/9a26c389-e669-4983-8c00-8c94629444c3)
![12](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/5983ccf0-2022-41f2-8c0e-9e87d9626c67)
![11](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/41762104-34e1-46d8-adc8-b845239fd0dd)
![10](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/aecbfc70-4b3a-43f9-85b7-40ecb9c1da68)
![9](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/94f2f30b-1a97-44e1-9b7c-936b1b741f94)
![8](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/783bcf75-134a-4673-830e-1d9c6243162e)
![7](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/fbed314f-62a4-4575-8c07-6897d4d82d08)
![6](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/4c5b9df8-1980-4bf1-88b5-33e14c731c74)
![5](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/1b7efc15-c096-4baa-8a0e-a00d39b1ce5f)
![4](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/df4df6fb-ff29-409c-ae56-eda2c0d0b2ef)
![3](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/bef195cc-d7f0-4327-8a83-e3e277286ec6)
()
.png…]()


## 개발일정   
<img src ="https://user-images.githubusercontent.com/64457004/95589062-2f8fa700-0a7f-11eb-85b3-439a412f62b1.png" width="600px"/>

## 기능정의서 中
<img src ="https://user-images.githubusercontent.com/64457004/95589066-328a9780-0a7f-11eb-9f5d-522d510e2b43.png" width="600px"/>  

## 디렉토리 정의서 中
<img src ="https://user-images.githubusercontent.com/64457004/95589073-34ecf180-0a7f-11eb-86b5-22522a98b1ec.png" width="600px"/>  

## 테이블 정의서 中
<img src ="https://user-images.githubusercontent.com/64457004/95589080-38807880-0a7f-11eb-9478-5fc00bf0ec28.png" width="600px"/>

## Coding Rule  
0. 회의시간 9:30~10:00
1. Controller마다 Data가 넘어오면 println으로 찍어놓기 - 형식(DataName=value)
2. coding Branch == master/ys/boo62/product/jahoon/209
3. Git push는 하나의 로직처리시 마다 단톡에 이야기 하고 push
4. pull은 매일 오전10:00 13:00 18:00 에 정기적으로, 상시pull은 단톡에 push가 올라오면 pull
5. 조장은 매일 20:00에 master와 branch를 merge하여 master에 Push
6. DAO는 DAO/DAOImpl 구조로 명명및 작성
7. UrlMapping과 Method이름을 일치시킨다

## Url 정리
Default localhost:8080/
## 디렉토리 구조
java/.../aop=AOP 
java/.../bean=chat/csv/fileDown/kakaoAPI/
			  CommonInterFace/JsonUtil/LowerHashMap/Pager  
			  
###Module      
java/.../module*/dao=DAO interface/class  
java/.../module*/vo=DTO  
java/.../module*/mvc=Controller  
java/.../module*/service=service  	
java/.../module*/sql=mybatis mapper xml    
WEB-INF/spring =servlet-context.xml을 제외한 모든 xml설정파일 
WEB-INF/views/tiles/*=layout관련 tileSetting파일

## AOP
memberAspect 쿠키/세션/관리자 검사   
Project.spring.aop.MemberAspect proceed를 기준으로 Session, Cookie검사및 Mapping method log 작성  
메소드이름 Ss로 끝내면 세션검사->로그인폼으로이동 AOP처리

## Spring tiles
ViewResolver String Return시에 "*.mn" 로 리턴시 template의 body

## Git을 다루면서 일어나는 문제들에 대한 Tip

## log4j
log4j.xml의 위치==src/main/resource/log4j.xml 

## Util 정리
### Pager(예제파일 : Project.spring.beans.example)
1. Pager AutoWired 이후, Pager Class의 pager(int PageNum,int count)를 사용할것  
2. controller에서 게시물 리스트 가져올때 사용법  articleList=boardDAO.getArticle(pageVO.getStartRow(),pageVO.getEndRow()) 
3. View에서 사용법 <c:if test="${pageVO.startPage > pageVO.pageBlock}"></c:if>

