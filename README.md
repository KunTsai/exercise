- __競賽題1:__
```CSS
const abc= () => {
  const a = 1;
  const b = 2;
  const c = 3;
  console.log(`a是:${a} b是:${b} c是:${c}`)
};
abc();
```

- __競賽題2:__
```CSS
function print(input){
  if(input===0)
    console.log("0");
  else if(input>0)
    console.log("正數");
  else
    console.log("負數");
}
print(0)
```

- __競賽3:__
```CSS
<!DOCTYPE html>
<html lang="zh-Hant">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        .mypage{
            color:red;
        }

        @media screen and (min-width: 1024px) {
            .mypage {
                color: red;
            }
        }

        @media screen and (min-width: 350px) and (max-width: 1024px){
            .mypage {
                color: blue;
            }
        }
    </style>
</head>

<body>

    <p class="mypage">我的網頁</p>

</body>

</html>
```

- __競賽題4:__
```CSS
<!DOCTYPE html>
<html lang="zh-Hant">

<head>
</head>

<body>

    <img id='img' src="https://fakeimg.pl/150x130" >
    <button id='btn1'>顯示圖片</button>
    <button id='btn2'>隱藏圖片</button>

</body>

<script>
const img = document.getElementById('img');
const btn1 = document.getElementById('btn1');
const btn2 = document.getElementById('btn2');

btn1.onclick = function () {
      img.style.display = 'block';
}

btn2.onclick = function () {
      img.style.display = 'none';
}
</script>
</html>
```

- __競賽題5:__
```CSS
<!DOCTYPE html>
<html lang="zh-Hant">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>

<body>

    <div id='label'>我的網頁</div>
    <button id='btn1'>黑</button>
    <button id='btn2'>藍</button>

</body>

<script>
    document.getElementById('btn1').addEventListener('click', function () {
        document.getElementById('label').style.color = 'black';
    });

    document.getElementById('btn2').addEventListener('click', function () {
        document.getElementById('label').style.color = 'blue';
    });
</script>

</html>
```

- __競賽題6:__
```CSS
function printtree(treeHeight, treeGap) {
  let ans = "";
  const maxStar = 1 + (treeHeight - 1) * treeGap;

  for (let i = 0; i < treeHeight; i++) {
    const levelStar = 1 + i * treeGap;
    const levelDashes = (maxStar - levelStar) / 2;
    const levelStr = "-".repeat(levelDashes) + "*".repeat(levelStar) + "-".repeat(levelDashes);
    ans += levelStr + "\n";
  }
  return ans;
}

const treeHeight = 5;
const treeGap = 2; 
console.log(printtree(treeHeight, treeGap));
```

- __延伸題1:__
```CSS
const print=(x)=>{
    x%2==0 ? console.log("x是2的倍數") : console.log("x不是2的倍數")
}

print(5)
```

- __延伸題2:__
```CSS
const demo = (arr,index) => {
    arr.splice(index,1)//從index處刪除，且刪除1個元素
    return arr
}
console.log(demo(['a','b','c'],0))
```

- __延伸題3:__
```CSS
const convertDate = (date) => {
    const dateObj = new Date(date);
    const yearTw = dateObj.getFullYear() - 1911;
    const month = ('0' + (dateObj.getMonth() + 1)).slice(-2);
    const day = ('0' + dateObj.getDate()).slice(-2);
    return `${yearTw}/${month}/${day}`;
}

console.log(convertDate("2024-05-23 00:00:00"));
```

- __延伸題4:__
```CSS
const fruits = {
  Banana: {
    num: "一串",
    price: "50"
  },
  Orange: {
    num: "五顆",
    price: "100"
  },
  Apple: {
    num: "3顆",
    price: "50"
  }
};

Object.keys(fruits).forEach(fruit => {
  console.log(`${fruit}是${fruits[fruit].num}${fruits[fruit].price}元`)
});
```

- __延伸題5:__
```CSS
for (let i = 1; i <= 9; i++) {
  let line = ''; 
  for (let j = 1; j <= 9; j++) {
    line += `${i} * ${j} = ${i * j}  `; 
  }
  console.log(line);  
}
