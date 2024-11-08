# techeer-partners-api-session

## 1. 세션 레포지토리를 fork

![image](https://github.com/user-attachments/assets/87f043f3-4ef3-4856-90c8-388cc6e08d81)
![image](https://github.com/user-attachments/assets/9b8bede4-f129-425c-b641-4e111419b1df)

<p>Owner를 팀 organization으로 설정합니다.</p>
<p>레포지토리 이름을 변경하지 않아야 스프링 프로젝트가 제대로 인식됩니다!</p>

## 2. Git 세션을 참고하여 fork한 레포지토리를 clone

## 3. Docker Desktop 설치
<p>https://www.docker.com/products/docker-desktop/</p>
<p>위의 링크를 통해 본인 노트북에 맞는 Docker Desktop을 설치합니다.</p>

![image](https://github.com/user-attachments/assets/8ffa568f-fa3f-4a8e-bf37-48df1d75b38c)

## 4. Docker Desktop 실행
<p>설치한 Docker Desktop을 실행합니다. 회원가입과 로그인을 요구한다면 skip하셔도 무방합니다.</p>

![image](https://github.com/user-attachments/assets/335468d8-9f1d-447e-ad69-69f4ab7da19c)

## 5. docker-compose 빌드
<p>터미널을 통해 프로젝트의 루트 디렉토리로 이동합니다.</p>

![image](https://github.com/user-attachments/assets/f539b6de-d3ad-471d-b813-72a2ef97a5d6)

<p>터미널에 다음 명령어를 입력하여 도커 이미지를 빌드합니다.</p>

```bash
docker-compose up

# 버전에 따라 -를 제거한 다음 명령어를 쳐야할 수도 있습니다.
docker compose up
```

![image](https://github.com/user-attachments/assets/ec888f2d-2ccc-4268-af74-d4b96908ccb7)
<p>처음 빌드할 때는 시간이 오래 걸릴 수 있습니다.</p>

## 6. Docker Desktop 확인
![image](https://github.com/user-attachments/assets/2180df91-6793-4730-8939-9a96919130e5)
<p>위와 같이 컨테이너가 생성된 것이 보인다면 성공입니다.</p>
<p>8080:8080을 누르면 localhost:8080으로 접속됩니다</p>

![image](https://github.com/user-attachments/assets/f8ff0e25-74f4-4312-87a8-d899c85ab783)
<p>에러가 아닌 처음 스프링 서버를 실행했을 때의 기본 화면입니다.</p>

<br>

<p>이렇게 Docker Desktop만 설치해준다면 프론트엔드에서도 별도의 서버 프레임워크 설치 없이 서버를 구동할 수 있습니다.</p>

<br>

# 과제 요구사항

## 기본 요구 사항
<p>1. 할 일 추가 API 구현 (POST /tasks)</p>
<p>새로운 할 일을 생성하는 API를 구현합니다. 요청에는 title이 포함되어야 합니다.</p>
<br>
<p>2-1. 할 일 전체 목록 조회 API 구현 (GET /tasks)</p>
<p>할 일의 목록을 조회하는 API를 구현합니다.</p>
<br>
<p>2-2. 완료된 일 조회 API 구현</p>
<p>완료된 할 일만 조회할 수 있는 API를 구현합니다.</p>
<br>
<p>2-3. 미완료된 일 조회 API 구현 </p>
<p>아직 완료되지 않은 할 일만 조회할 수 있는 API를 구현합니다.</p>
<br>
<p>(2-2와 2-3은 별도의 API를 구현하셔도 되고 Query Parameter를 사용하셔도 무방합니다.)</p>
<br>
<p>3. 할 일 수정 API 구현 (PUT /tasks/{id} 또는 PATCH /tasks/{id})</p>
<p>특정 할 일의 내용을 수정할 수 있는 API를 구현합니다. 할 일의 제목인 title이나 완료 여부인 isDone을 수정합니다.</p>
<br>
<p>4. 할 일 삭제 API 구현 (DELETE /tasks/{id})</p>
<p>특정 할 일을 삭제 할 수 있는 API를 구현합니다.</p>

## Challenge (추가 도전 과제)</p>
<p>1. 유효성 검증: 요청 시 필수 필드가 누락되지 않도록 유효성을 검증하는 로직을 추가합니다.</p>
<p>2. 적절한 상태 코드와 응답 메시지: 요청 결과에 따라 적절한 상태 코드(예: 200 OK, 201 Created, 400 Bad Request, 404 Not Found)와 응답 메시지를 반환하도록 구현합니다.</p>
<p>3. Swagger 연동: Swagger를 사용하여 API를 문서화하고, 문서를 기반으로 API를 테스트할 수 있도록 합니다.</p>
<br>

### 이외의 추가 기능은 팀에서 자유롭게 회의하여 추가하셔도 됩니다
