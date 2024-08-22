# W10D4
> Day 4 of Docker
> 여러 컨테이너를 한 무대(네트워크)에 세우는 것

## SpringBoot
> @autowired 를 사용하는 이유는 Boot가 미리 만든 Bean 객체를 이용하기 위함. <br>
> > @required와 달리 존재하지않을 수 있으므로 반드시 존재해야하는 경우는 단위테스트로 존재여부를 확인. <br>

## SpringBoot를 컨테이너로 만들기
> ## Gradle Project 패키지 가져오기
> > 1. terminal 에서 `./gradlew clean build` 입력
> > 2. 새로 생성된 `build/libs/[프로젝트명]-SNAPSHOT.jar`를 이미지로 생성해야함
>
> ## Dockerfile 생성 및 작성
> > 3. 프로젝트 폴더 하위에 dockerfile 생성
> > 4. jar파일을 이미지로 만들기 위해서는 JAVA 이미지(openjdk)가 필요.
> > 5. FROM openjdk:[프로젝트 java 버전]
> > 6. ARG [변수명]=/build/libs/[프로젝트명]-SNAPSHOT.jar
> > > ARG : 변수 선언
> >
> > 7. COPY ${변수명} /[파일명].jar
> > > 변수를 사용하려면 ${변수명}을 이용한다.
> > > 위의 뜻은 ${변수명}에 해당하는 파일을 현재위치(/)에 [파일명]으로 복사
> >
> > 8. ENTRYPOINT [ "java", "-jar", "/[파일명].jar" ]
> > > tmp
> 
> 9. terminal에서 docker build -t doc_boot-img




## 네트워크 생성 및 연결
> 1. temp
