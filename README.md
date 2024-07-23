# php_vue3
php项目集成vue3 多页面应用

# 背景
早期使用yaf搭建的php后台管理系统，属于ssr，前端采用传统的jquery + bootstrap架构。
目前在这个基础上需要开发新功能。考虑到后期可能重构和维护性。 
- 需要把SSR架构调整为前后端分离
- 前端改用vue3+vite+elementPlus架构
- 数据获取从php输出改成resful风格访问，基于数据驱动，不在操作dom


# 方案1:  php + vue3多页面应用
直接在对应的php页面上写vue3的多页面应用
优点： 
1. 粗暴直接，直接引入cdn即可使用
2. 调试快，不用再构建
3. 使用cdn多次渲染，也不用重复再加载原来资源
   
缺点：
1. 复用的代码只能过用js引入，容易导致全局污染
2. 当页面多了，很难维护，无法做到组件化开发
3. 编写html的标签必须有闭合标签，不能简写，如  `<el-table-column label="姓名" align="center" prop="name" />`  将不会有意想不到的效果。
4. 后期如何要整体切换到spa应用调整成本也大

# 参考地址
https://juejin.cn/spost/7394622095773745190