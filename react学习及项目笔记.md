# react基础

## 一 基础语法

![image-20231021143202100](E:\学习资料\images\image-20231021143202100.png)

### 1.1函数式组件

![image-20231021150125758](E:\学习资料\images\image-20231021150125758.png)

### 1.2 类式组件

![image-20231021145921776](E:\学习资料\images\image-20231021145921776.png)

## 二 state

### 1.1 使用

![image-20231021150730625](E:\学习资料\images\image-20231021150730625.png)

### 1.2 setState

**修改state的值需要使用setState方式修改**

![image-20231021160409689](E:\学习资料\images\image-20231021160409689.png)

### 1.3 完整写法

![image-20231021161346536](E:\学习资料\images\image-20231021161346536.png)

### 1.4总结

![image-20231021161509819](E:\学习资料\images\image-20231021161509819.png)

## 二 props

### 1.1 使用

![image-20231021163400040](E:\学习资料\images\image-20231021163400040.png)

### 1.2 props的限制

![image-20231021164215125](E:\学习资料\images\image-20231021164215125.png)

简写形式

![image-20231021164455215](E:\学习资料\images\image-20231021164455215.png)

### 1.3 函数式组件使用props

![image-20231021165319559](E:\学习资料\images\image-20231021165319559.png)

## 四 refs

### 1.1 基本使用

字符串形式的refs **不建议使用**

![image-20231021170104278](E:\学习资料\images\image-20231021170104278.png)

### 1.2回调内联回调形式refs 建议使用

![image-20231021170729546](E:\学习资料\images\image-20231021170729546.png)

### 1.3 createRef 官方推荐

![image-20231021190452774](E:\学习资料\images\image-20231021190452774.png)

## 五 事件处理

![image-20231021191030402](E:\学习资料\images\image-20231021191030402.png)

![image-20231021191228850](E:\学习资料\images\image-20231021191228850.png)

### 1.1受控组件：输入类的DOM的值报错在state中就是受控组件 非受控组件则反之

### 1.2 高阶函数  函数科里化

![image-20231021193739357](E:\学习资料\images\image-20231021193739357.png)

![image-20231021192637791](E:\学习资料\images\image-20231021192637791.png)

把上面优化为如下 saveFormData就是高阶函数 和应用了函数科里化

![image-20231021193410087](E:\学习资料\images\image-20231021193410087.png)

不用函数柯里化实现 如下

![image-20231021194340127](E:\学习资料\images\image-20231021194340127.png)

## 六 生命周期

![image-20231021200241144](E:\学习资料\images\image-20231021200241144.png)

![image-20231021211347311](E:\学习资料\images\image-20231021211347311.png)

![image-20231021195920270](E:\学习资料\images\image-20231021195920270.png)

新生命周期

![image-20231021213051792](E:\学习资料\images\image-20231021213051792.png)

![image-20231022003156722](E:\学习资料\images\image-20231022003156722.png)

![image-20231022003045865](E:\学习资料\images\image-20231022003045865.png)

## 七diffing算法

![image-20231022153208305](E:\学习资料\images\image-20231022153208305.png)

![image-20231022154144908](E:\学习资料\images\image-20231022154144908.png)

# 搭建项目

## 一 项目初始化

### 1.1 使用npm安装

安装指令

```
npx create-react-app xxx
```

### 1.2 子组件传值给父组件

父组件App.jsx传递函数addTodo给子组件 

![image-20231022174842959](E:\学习资料\images\image-20231022174842959.png)

子组件调用该函数并传递参数

![image-20231022175230493](E:\学习资料\images\image-20231022175230493.png)

实现鼠标移入移出显示高亮

![image-20231022203949107](E:\学习资料\images\image-20231022203949107.png)

### 1.3 跨域配置

![image-20231022223209771](E:\学习资料\images\image-20231022223209771.png)

**注意**

![image-20231022223225262](E:\学习资料\images\image-20231022223225262.png)

### 1.4 兄弟组件通信

**使用消息订阅-发布功能实现**

使用基于上述原理pubsubjs 库实现

```
npm i pubsub-js
```

订阅消息

![image-20231022232402786](E:\学习资料\images\image-20231022232402786.png)

发布消息

![image-20231022232454506](E:\学习资料\images\image-20231022232454506.png)

## 二 路由及原理

### 1.1有history和hash两种模式

![image-20231025231128268](E:\学习资料\images\image-20231025231128268.png)

![image-20231023205323604](E:\学习资料\images\image-20231023205323604.png)

![image-20231023205433907](E:\学习资料\images\image-20231023205433907.png)

### 1.2  react-route-dom5的基本使用

![image-20231023210319457](E:\学习资料\images\image-20231023210319457.png)

![image-20231023221649428](E:\学习资料\images\image-20231023221649428.png)

路由组件和一般组件的不同

![image-20231023222731648](E:\学习资料\images\image-20231023222731648.png)

### 1.3 封装NavLink 及 Switch的使用

![image-20231023225107260](E:\学习资料\images\image-20231023225107260.png)

**使用**

![image-20231023230422259](E:\学习资料\images\image-20231023230422259.png)

### 1.4路由的模糊匹配和严格匹配

默认为模糊匹配 exact设置为true开启严格匹配

![image-20231023232057013](E:\学习资料\images\image-20231023232057013.png)

![image-20231023231855214](E:\学习资料\images\image-20231023231855214.png)

### 1.5 Redirect的使用

**注意 其他路由放在Redirect前面 否则不会渲染**

![image-20231023232918079](E:\学习资料\images\image-20231023232918079.png)

### 1.6 嵌套路由

![image-20231024221108229](E:\学习资料\images\image-20231024221108229.png)

![image-20231024221016739](E:\学习资料\images\image-20231024221016739.png)

### 1.7 路由传参方式 

#### 1.7.1通过params传递参数

**传递**参数

![image-20231024223448470](E:\学习资料\images\image-20231024223448470.png)

**接收**参数

![image-20231024223727534](E:\学习资料\images\image-20231024223727534.png)

![image-20231024224133616](E:\学习资料\images\image-20231024224133616.png)

#### 1.7.2 通过search传递参数

**传递**参数

![image-20231024225854915](E:\学习资料\images\image-20231024225854915.png)

执行命令

```
npm i query-string
```

**接收**参数

![image-20231024225828950](E:\学习资料\images\image-20231024225828950.png)

#### 1.7.3 通过state传递参数

**传递**参数

![image-20231024230507419](E:\学习资料\images\image-20231024230507419.png)

**接收**参数

![image-20231024230801358](E:\学习资料\images\image-20231024230801358.png)

### 1.8 路由跳转方式 

默认开启push模式 会在浏览器留下记录

开启replace模式如下

**在哪个路由中开启，这个路由就不会浏览器中留下记录**

![image-20231024232317391](E:\学习资料\images\image-20231024232317391.png)

### 1.9 路由导航编程

![image-20231025000719120](E:\学习资料\images\image-20231025000719120.png)

方法

![image-20231025000736965](E:\学习资料\images\image-20231025000736965.png)

![image-20231025001450406](E:\学习资料\images\image-20231025001450406.png)

### 2.0 withRouter

**注意 只有路由组件才会想this.props传递history 一般组件this.props中没有history对象**

通过withRouter加工一般组件 是的一般组件能使用history对象

![image-20231025230900868](E:\学习资料\images\image-20231025230900868.png)

## 三 ui组件库的使用

![image-20231025231946882](E:\学习资料\images\image-20231025231946882.png)

# 四 redux

## 1 原理

![image-20231026212958514](E:\学习资料\images\image-20231026212958514.png)

## 1.2 使用redux

执行命令 

```
npm i redux
```

## 1.3 在src下创建redux文件夹

​	在redux文件夹中创建store.js文件 写入以下内容

​	![image-20231026234751879](E:\学习资料\images\image-20231026234751879.png)

## 1.4 精简版

### 1在redux文件夹中创建count_Reducer.js文件 写入以下内容

![image-20231026235108130](E:\学习资料\images\image-20231026235108130.png)

### 2 在需要的组件导入并使用

![image-20231027223823563](E:\学习资料\images\image-20231027223823563.png)

### 3在入口文件index.js进行监听

![image-20231027225623237](E:\学习资料\images\image-20231027225623237.png)

 **总结**

![image-20231027230113844](E:\学习资料\images\image-20231027230113844.png)

## 1.5 完整版

### 1在redux文件夹中创建contant.js文件  目的防止写错字符相关的变量

![image-20231027231830015](E:\学习资料\images\image-20231027231830015.png)

### 2 在redux文件夹中创建count_action.js文件

![image-20231027231932443](E:\学习资料\images\image-20231027231932443.png)

### 3 将要使用的常量导入所需的文件中使用 如下

![image-20231027232112869](E:\学习资料\images\image-20231027232112869.png)

![image-20231027232142072](E:\学习资料\images\image-20231027232142072.png)

### 4 在Count组件中使用count_action.js

![image-20231027232401389](E:\学习资料\images\image-20231027232401389.png)

## 1.6 处理异步action

使用中间件 执行命令

```
npm i redux-thunk
```

在store.js中导入

![image-20231028000357285](E:\学习资料\images\image-20231028000357285.png)

**下图中count_action.js文件中的异步action要处理异步问题 就需要返回的是个函数 为了处理这个函数 需要以上中间价**

![image-20231028000316667](E:\学习资料\images\image-20231028000316667.png)

# 五 react-redux

## 1原理

![image-20231030215113850](E:\学习资料\images\image-20231030215113850.png)

## 1.2 使用react-redux

执行命令

```
npm i react-redux
```

在src文件夹中创建containers文件夹用于存放容器组件 创建Count文件夹 为Count的UI组件创建容器组件 写入以下内容

![image-20231030221727883](E:\学习资料\images\image-20231030221727883.png)

在app.js中容器组件代替ui组件使用 并传入store

![image-20231030222414090](E:\学习资料\images\image-20231030222414090.png)

## 1.3 基本使用

在容器组件中写入如下代码

![image-20231030225454166](E:\学习资料\images\image-20231030225454166.png)

上面可有优化成如下写法

![image-20231030230303757](E:\学习资料\images\image-20231030230303757.png)

在ui组件中调用 如下

![image-20231030225538004](E:\学习资料\images\image-20231030225538004.png)

**使用react-redux的优化**

在app.js文件中

![image-20231030231234329](E:\学习资料\images\image-20231030231234329.png)

在index.js入口文件中

![image-20231030231326445](E:\学习资料\images\image-20231030231326445.png)

## 1.4 多个组件共享全局状态 数据共享

将redux中的文件优化成如下结构

![image-20231030232817261](E:\学习资料\images\image-20231030232817261.png)

在constant.js中添加如下常量

![image-20231031003319052](E:\学习资料\images\image-20231031003319052.png)

在container文件夹中创建如下文件 Person/index.jsx 写入如下代码

![image-20231031002957819](E:\学习资料\images\image-20231031002957819.png)

在redux文件夹中分别创建如下文件

![image-20231031003101546](E:\学习资料\images\image-20231031003101546.png)

在action文件夹中的person.js文件中写入如下代码

![image-20231031003147976](E:\学习资料\images\image-20231031003147976.png)

在reducers文件夹中的person.js写入如下代码

![image-20231031003234774](E:\学习资料\images\image-20231031003234774.png)

将store.js文件修改为如下

![image-20231031003400876](E:\学习资料\images\image-20231031003400876.png)

将containers中的Count组件修改如下红圈部分

![image-20231031003835334](E:\学习资料\images\image-20231031003835334.png)

# 六 纯函数

![image-20231031230616318](E:\学习资料\images\image-20231031230616318.png)

# 七 redux开发者工具

## 1 在谷歌应用商店下载 Redux DevTools

![image-20231031231936216](E:\学习资料\images\image-20231031231936216.png)

## 2 在项目中安装插件

### 2.1执行命令

```
npm i redux-devtools-extension -D
```

### 2.2 在store.js文件中添加如下代码

![image-20231031232650684](E:\学习资料\images\image-20231031232650684.png)

# 八 hooks及扩展

## 1 state 写法

![image-20231031235550538](E:\学习资料\images\image-20231031235550538.png)

对象是写法如下

![image-20231101000012551](E:\学习资料\images\image-20231101000012551.png)

函数式写法如下

![image-20231101000410318](E:\学习资料\images\image-20231101000410318.png)

## 2 路由懒加载

![image-20231101000504151](E:\学习资料\images\image-20231101000504151.png)

具体使用如下 

![image-20231101000813190](E:\学习资料\images\image-20231101000813190.png)

![image-20231101001036794](E:\学习资料\images\image-20231101001036794.png)

![image-20231101001018339](E:\学习资料\images\image-20231101001018339.png)

## 3 hooks

![image-20231107225303046](E:\学习资料\images\image-20231107225303046.png)

### 1 useState

![image-20231107225921245](E:\学习资料\images\image-20231107225921245.png)

例子如下

![image-20231107230110459](E:\学习资料\images\image-20231107230110459.png)

**注意 useState要按照顺序执行 不能放在条件语句中**

### 2 useEffect

![image-20231107231017857](E:\学习资料\images\image-20231107231017857.png)

例子如下

![image-20231107233445272](E:\学习资料\images\image-20231107233445272.png)

### 3 useRef

![image-20231107234039633](E:\学习资料\images\image-20231107234039633.png)

例子如下

![image-20231107234014599](E:\学习资料\images\image-20231107234014599.png)

### 4 useContext 解决多层传值问题

在父组件使用

![image-20231115234010190](E:\学习资料\images\image-20231115234010190.png)

在子组件或后代组件中

![image-20231115234113556](E:\学习资料\images\image-20231115234113556.png)

### 5 useReducer

![image-20231115234840066](E:\学习资料\images\image-20231115234840066.png)

### 6 useReducer和useContext的结合使用代替redux

![image-20231116000106356](E:\学习资料\images\image-20231116000106356.png)



![image-20231116000341645](E:\学习资料\images\image-20231116000341645.png)

![image-20231116000415337](E:\学习资料\images\image-20231116000415337.png)

![image-20231116000430782](E:\学习资料\images\image-20231116000430782.png)

![image-20231116000454614](E:\学习资料\images\image-20231116000454614.png)

![image-20231116000600795](E:\学习资料\images\image-20231116000600795.png)

### 7 useMemo优化React Hooks程序性能

![image-20231116001515621](E:\学习资料\images\image-20231116001515621.png)

![image-20231116001527344](E:\学习资料\images\image-20231116001527344.png)

解决如下

![image-20231116001556942](E:\学习资料\images\image-20231116001556942.png)



### 8 自定义hooks函数

![image-20231116003037001](E:\学习资料\images\image-20231116003037001.png)

![image-20231116003048377](E:\学习资料\images\image-20231116003048377.png)

### 9 useSelector和useDispatch

![image-20231207000833589](E:\学习资料\images\image-20231207000833589.png)

**使用useSelector获取store中的数据 使用useDispatch修改仓库数据** 

修改优化成如下

![image-20231207000229135](E:\学习资料\images\image-20231207000229135.png)

![image-20231207215056218](E:\学习资料\images\image-20231207215056218.png)

优化reducer如下

![image-20231207222435549](E:\学习资料\images\image-20231207222435549.png)

优化模块化数据如下

![image-20231207222733412](E:\学习资料\images\image-20231207222733412.png)

**使得最终的用法类似vuex**

![image-20231207223711297](E:\学习资料\images\image-20231207223711297.png)

## 4 Fragment

![image-20231107234142715](E:\学习资料\images\image-20231107234142715.png)

## 5 Context

![image-20231107234625096](E:\学习资料\images\image-20231107234625096.png)

![image-20231107235921451](E:\学习资料\images\image-20231107235921451.png)

例子如下 在类式组件中使用

![image-20231107235347565](E:\学习资料\images\image-20231107235347565.png)

![image-20231107235653310](E:\学习资料\images\image-20231107235653310.png)

![image-20231107235552511](E:\学习资料\images\image-20231107235552511.png)

在函数式组件中使用

![image-20231107235813843](E:\学习资料\images\image-20231107235813843.png)

## 6 pureComponent  组件优化

![image-20231108224543534](E:\学习资料\images\image-20231108224543534.png)

![image-20231108231155399](E:\学习资料\images\image-20231108231155399.png)

使用方法如下

![image-20231108225310689](E:\学习资料\images\image-20231108225310689.png)

## 7 renderProps

![image-20231108232324410](E:\学习资料\images\image-20231108232324410.png)

**相当于vue中的插槽技术**

![image-20231108232107124](E:\学习资料\images\image-20231108232107124.png)

## 8 errorboundary 错误边界

![image-20231108233656005](E:\学习资料\images\image-20231108233656005.png)

使用如下

![image-20231108233735855](E:\学习资料\images\image-20231108233735855.png)

## 9 通信方式总结

![image-20231108233937289](E:\学习资料\images\image-20231108233937289.png)

# 九 react router 6

## 一 安装

执行命令

```
npm i react-router-dom
```

## 二  BrowserRouter

![image-20231109000052071](E:\学习资料\images\image-20231109000052071.png)

## 三 HashRouter

![image-20231109000139594](E:\学习资料\images\image-20231109000139594.png)

## 四  Routes 和Route

![image-20231109000330401](E:\学习资料\images\image-20231109000330401.png)

**使用useRoutes生成路由表**

![image-20231109001058378](E:\学习资料\images\image-20231109001058378.png)

![image-20231109001158046](E:\学习资料\images\image-20231109001158046.png)

**嵌套路由表**

![image-20231109001703818](E:\学习资料\images\image-20231109001703818.png)

**路由呈现位置 占位作用**

![image-20231109001808015](E:\学习资料\images\image-20231109001808015.png)

## 五 Link

![image-20231109001351466](E:\学习资料\images\image-20231109001351466.png)



## 六  NavLink

![image-20231109004208711](E:\学习资料\images\image-20231109004208711.png)

![image-20231109004224757](E:\学习资料\images\image-20231109004224757.png)

自定义高亮效果

![image-20231109000840737](E:\学习资料\images\image-20231109000840737.png)

## 七 Navigate

![image-20231109000236721](E:\学习资料\images\image-20231109000236721.png)

## 八 路由传参

### 1 params 

![image-20231109002209508](E:\学习资料\images\image-20231109002209508.png)

![image-20231109002248191](E:\学习资料\images\image-20231109002248191.png)

![image-20231109002352662](E:\学习资料\images\image-20231109002352662.png)

### 2 search

![image-20231109002508600](E:\学习资料\images\image-20231109002508600.png) 

![image-20231109002550236](E:\学习资料\images\image-20231109002550236.png)

![image-20231109002720152](E:\学习资料\images\image-20231109002720152.png)

### 3 state

![image-20231109002852512](E:\学习资料\images\image-20231109002852512.png)

![image-20231109002940877](E:\学习资料\images\image-20231109002940877.png)

![image-20231109003022624](E:\学习资料\images\image-20231109003022624.png)

##  九 编程式路由导航

### 一 useNavigate

![image-20231109003559528](E:\学习资料\images\image-20231109003559528.png)

**注意  params和search 参数在编程式路由导航中只能直接拼接在路由中**

### 二 useInRouterContext

![image-20231115221151252](E:\学习资料\images\image-20231115221151252.png)

### 三 useNavigationType

![image-20231115221322139](E:\学习资料\images\image-20231115221322139.png)

### 四 useOutlet

![image-20231115221511847](E:\学习资料\images\image-20231115221511847.png)

### 五 useResolvedPath

![image-20231115221540129](E:\学习资料\images\image-20231115221540129.png)

## 十 总结

