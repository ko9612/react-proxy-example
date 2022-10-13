# react-proxy-example
This is an example project on how to proxy to backend servers in React Applications

<br>

## Bare Minimum Requirement
<br>
여기 레포지토리로 들어가 `git clone` 한 뒤, 과제를 진행합니다.

<br>

백엔드의 개발 서버 역할을 해줄 api와, 클라이언트의 개발 서버 역할을 해줄 my-app에 각각 접근하여 `npm install`을 합니다.
`cd api`
<br>
`npm install`
<br>

`cd my-app`
<br>
`npm install`

<br>
백엔드와 클라이언트 각각 `npm install`을 할 시, 터미널 각각 따로 열어 npm install을 해줘야 데이터 요청 흐름을 확인하기 편합니다.

<br>

이어 api에 접근한 터미널에서는 `npm run dev`를, my-app에 접근한 터미널에서는 `npm start`를 통해 각기 개발 서버를 엽니다.

<br>

//api terminal<br>
```npm run dev```

//my-app terminal<br>
```npm start```

그러면 터미널이 각기 이런 화면으로 여러분을 맞이할 것입니다.


<br>


![image](https://user-images.githubusercontent.com/75575781/195524559-0c3a68df-0e54-4ecd-97e6-f705075c27ad.png)

[그림] 백엔드 API 개발 서버가 구동 중인 터미널

<br>

![image](https://user-images.githubusercontent.com/75575781/195524618-514a58b7-bf75-40a9-b85c-a1d771874604.png)

[그림] 클라이언트 개발 서버가 구동 중인 터미널

<br>

이 상태에서 Get all Books 라고 쓰여 있는 버튼을 눌러 봅시다.

![image](https://user-images.githubusercontent.com/75575781/195524661-95e1fca5-9299-43de-91ef-1cc095160ed4.png)

[그림] CORS 에러가 뜨는 콘솔창

<br>

CORS 에러가 뜨며 응답을 제대로 받아오지 못하는 것을 확인할 수 있습니다. 여러분은 이 단계에서부터 proxy 기능을 사용해 페어와 함께 CORS 에러를 해결해 나갈 것입니다.

<br><br>

###과제1
페어와 함께 webpack dev server의 proxy 기능을 사용해 우회하여 응답을 받아옵니다.

<br>

### 과제2
레포지토리로 받아온 과제를 살펴보면 api2 라는 폴더가 존재하고 있습니다. 실제로 프로젝트 및 실무를 할 때, 하나의 도메인이 아닌 여러 개의 도메인에서 응답을 받아와야 하는 경우가 종종 있습니다. 이럴 때는 유연하게 proxy를 설정할 필요가 있습니다.

+ 페어와 함께 webpack dev server의 proxy 기능 대신 http-proxy-middleware의 proxy 기능을 사용하여 proxy를 유연히 설정해 2개의 도메인에서 모두 응답을 받아옵니다.
+ 페어와 함께 api2에 관련된 fetch 함수를 만들고, 컴포넌트를 하나 이상 만들어 2개의 도메인에서 모두 응답을 받아오는지 테스트 해봅니다.

