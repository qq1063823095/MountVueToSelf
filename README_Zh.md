# 用处
该脚本用于在 Tampermonkey 插件中使用 "@require" 方式引入 Vue 框架时使用

# 说明
某些三方框架(例如：Element Plus|)，会依赖Vue框架，在通过 "@require" 方式引入这些框架时，由于油猴脚本的执行方式限制，会导致框架中无法传入Vue对象，从而导致vue对象不存在而报错，具体如图所示：



![Alternative frameworks access the Vue instance within the window](./Images/Alternative%20frameworks%20access%20the%20Vue%20instance%20within%20the%20window.png)
![Function for executing scripts in Tampermonkey](./Images/Function%20for%20executing%20scripts%20in%20Tampermonkey.png)

# 其它
### 问：为什么不直接使用"WebPack"或"Vite"等打包工具将框架一同打包到脚本中？
### 答：因为最终打包的代码会很大，从而导致 Tampermonkey 插件卡死无法使用
