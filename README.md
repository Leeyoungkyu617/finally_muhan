## 주요 구현 기능  
[SpringMVC]     
[myBatis]  
[Ajax]  
[log4j]  

## 개발완료 시연 주요 화면

<img src="https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/2166394b-f1a3-434f-a4d4-0b5dcf68aafc" width="600px"/>  

![1](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/2166394b-f1a3-434f-a4d4-0b5dcf68aafc)
![2](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/2b517087-6f4a-48e0-861d-579f08961029)
![3](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/cb6dbe71-5d2c-4a97-8162-2a2718ca63b5)
![4](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/eb8ae775-c850-4d1d-8ea7-7f1cb4da3b8c)
![5](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/a8f5b0b5-96e5-49d7-83a6-623fa737b202)
![6](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/79eb7ffc-d2df-4401-a37d-e2cda455bbac)
![7](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/cc3853d6-6e7c-48b0-8da3-5af9c8bd8f90)
![8](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/20a17342-6618-4ba2-9423-aa56b754e8b4)
![9](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/65e0de72-bc68-43a9-9792-0282385c0fa6)
![10](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/3168a3ff-462b-4ece-9db6-218e8873f217)
![11](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/b01d3744-8ff9-487d-86d8-522262383210)
![12](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/19aa5ac5-29a2-45c9-98c1-0108be838afc)
![13](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/1d872449-36e0-42f1-ba32-4d36b676f212)
![14](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/71b3d5ab-fc66-4a43-bcec-6071257b4f64)
![15](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/b7144f8e-1f2a-4f08-a289-d07409219ed9)



## 개발일정   
![개발일정](https://github.com/Leeyoungkyu617/finally_muhan/assets/70137249/5ae1041c-305b-4ef4-9c56-48190cf1e01f)


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

