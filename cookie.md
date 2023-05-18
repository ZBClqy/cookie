# 前端操作Cookie

首先前端对于cookie的操作少之又少，下面我们就来完成一些常规的操作吧

## 插入cookie

document.cookie='cookie名称=cookie内容;'

多个cookie也是按此格式依次插入

## 删除cookie

document.cookie='cookie名称=0;expires='+new Date(0).toUTCString()

多个cookie也是按此格式依次插入

## 查询cookie

let cokArr=document.cookie.split(';')

let obj={}

for(let i=0;i<cokArr.length;i++){

​	let arr=cokArr[i].split('=')

​	obj[arr[0].trim()]=arr[1]

}

console.log(obj)

最后obj内就存储了所有的cookie