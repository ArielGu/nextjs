1. 项目初始化

mkdir next-demo
cd next-demo
npm init -y
npm install --save next react react-dom
mkdir pages

2. 脚本命令添加 package.json
{
  "scripts": {
    "dev": "next",
    "build": "next build",
    "start": "next start"
  }
}


==> 知识点：

  -next 基于react16；

  -npm init -y 跳过询问项创建package.json

  -nextjs 从服务器返回渲染好的页面（读取pages目录下的页面）

2. 路由遮盖：
   Link 标签的as 属性（实质是修改浏览器中的url，路由识别还是遮盖前的）
  问题：页面刷新导致404，需要在服务器端实现路径反解析
  解决方法详见：server.js

3. css in js
  nextjs 中支持css in js 的特性，使用 <style jsx> 标签 <style jsx>{` ... `}</style>。其实nextjs是使用babel 插件解析

  **需要注意的是：style-jsx 的样式不会应用到子组件，如果想要该样式适用于子组件，可以在 style-jsx 标签添加属性 global：<style jsx global>。**
