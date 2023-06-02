# Github.io로 배포하기
1. 먼저 프로젝트에 ```gh-pages``` 패키지 설치
```
npm install gh-pages --save-dev
```
2. 설치 완료후 프로젝트에 있는 ```package.json``` 파일을 열어 'homepage'주소 추가
형식은 ```http://{user name}.github.io/{repository name}```
```
{
    // ...
    "homepage": "http://hn04147.github.io/sample-react-app",
}

```
3. ```script``` 부분에 ```predeploy, deploy``` 추가
```
"scripts": {
    //...
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build"
}
```
4. 저장하고 터미널을 열어 ```npm run deploy``` 실행