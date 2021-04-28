let html = document.querySelector("#html"); //在HTML创建一个demo元素，通过css找到这个元素，querySelector（通过css找到某个元素）
let style = document.querySelector("#style");
let string = `
/*你好，我是一名前端新人
*接下来我演示一下我的前端功底
*首先我要准备一个div
**/
#div1{
    border: 1px solid red;
    width: 200px;
    height: 200px;
}
/* 接下来我把div变成一个太极
*注意看好了
*首先把div变成一个圆
**/
#div1{
    box-shadow:0 0 3px rgba(0,0,0,0.5);
    border-radius: 50%;
    border: none;
}
/* 太极一黑一白
**/
#div1{
    background: linear-gradient(90deg, rgba(255,255,255,1) 50%, rgba(0,0,0,1) 50%, rgba(0,0,0,1) 50%);
}
/* 加两个神秘的小球*/
#div1::before{
    width: 100px;
    height:100px;
    left:50%;
    transform: translateX(-50%);
    background:#000;
    border-radius:50%;
    background: radial-gradient(circle, rgba(0,0,0,1) 25%, rgba(255,255,255,1) 25%, rgba(255,255,255,1) 100%);
}
#div1::after{
    width: 100px;
    height:100px;
    bottom:0;
    left:50%;
    transform: translateX(-50%);
    background:#fff;
    border-radius:50%;
    background: radial-gradient(circle, rgba(255,255,255,1) 25%, rgba(0,0,0,1) 25%, rgba(0,0,0,1) 25%);
}

`;
//加注释/*是为了让css在html里生效
let string2 = "";
let n = 0;
let step = () => {
  setTimeout(() => {
    if (string[n] === "\n"){
        string2 += "<br>";//当第n个为回车时打印出<br>
    }else if (string[n] === " "){
        string2 += "&nbsp;";//当第n个为空格时打印出&nbsp;
    } else {
        string2 += string[n];// 继续打印string内容
    }
    html.innerHTML = string2;
    style.innerHTML = string.substring(0, n);//substring() 方法返回一个字符串在开始索引到结束索引之间的一个子集, 或从开始索引直到字符串的末尾的一个子集。
    window.scrollTo(0,99999);
    html.scrollTo(0,99999);
    if (n < string.length - 1) {
      n += 1;
      step();
    }
  }, 50);
};

step();
