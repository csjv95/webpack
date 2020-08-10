# Loader error & Why need loader?
<strong>loader는 순서에 영향을 받으며 오른쪽에서 왼쪽으로 순서대로 적용이된다</strong>


## 오류 없는 결과
```
module: {
    rules: [
      {
        test: /\.css$/,
        use: ['style-loader', 'css-loader']
      }
    ]
  },
}
```  
![loader](./imgs/loader-error1.PNG);


### 오류 1
위치만 바꿔는데 오류가 생겼다 
![error](./imgs/loader-error2.png);

### 오류 2
css-loder만 하면 오류는 생기지 않았다 

![error](./imgs/loader-error3.png);  

하지만 style이 없어서 적용했던 color : orange가 적용 되지 않는다  
![error](./imgs/loader-error4.png);

## loader report
> 위 오류를 보면 알수 있듯이 loader는 순서에 영향을 받으며 오른쪽에서 왼쪽으로 순서대로 적용이된다 그리고 실행 결과와 오류를 보면 알수 있듯이 loader는 웹 애플리케이션을 해석할때 자바스크립트가 아닌 파일에 대해서 웹 펙으로 변한할수 있게 적용해주는 속성이다
