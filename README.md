# 별말, 씀

### Introduce
서비스 기간 2022.09.02. ~ 2022.09.22. <br>
현재 서비스 종료 <br>
별말, 씀은 모바일 웹 기반 애플리케이션으로 롤링페이퍼를 작성해 서로 하말고 싶은 메세지를 주고 받을 수 있는 애플리케이션입니다.
<br>
노션 페이지 - https://www.notion.so/6435598d99634b4d88de9983ea12df43

###  how to run project

1. `git clone https://github.com/pullingoff/jtm-fe.git` : 깃허브 저장소 클론
2. `yarn install` : package.json 기반으로 파일 의존성 설치
   - node version : 16
3. `yarn start`: tsc-watch가 .ts를 .js로 컴파일한 후 변환에 모두 성공하면 `react-script start`
4. 추후 repo 에 내용이 업데이트 되면
   - `git pull`
   - `npm run start`

<br>

### 라이브러리 부가설명

- `tsc-watch`: ts 파일이 변경되는 걸 감시하면서 내용이 바뀔 때마다 js로 변환
- `node-sass`: .scss를 사용하기 위해 필요
- `styled-component`: CSS in JS, 재사용하기 편한 styled 컴포넌트를 만듦

- `npm i -D typescript @babel/core @babel/preset-env @babel/preset-typescript @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint prettier eslint-plugin-prettier`: eslint를 사용할 때 install 해줘야 하는 목록들 

<br>

### 로그인 저장 정보

> email: 'star_horse_write@gmail.com', password: '12345678',

- 로그인 성공 시 저장하는 정보

1. localStorage
```js
currentUser {
   id(idToken), 
   userName(닉네임),
   email
}
```
2. authContext (useContext로 사용가능)
```js
user {
   userName,
   email
}, 
token
```
