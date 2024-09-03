## hooks

![image-20231107225303046](.\images\image-20231107225303046.png)

## 1 useState

![image-20231107225921245](.\images\image-20231107225921245.png)

例子如下

![image-20231107230110459](.\images\image-20231107230110459.png)

**注意 useState要按照顺序执行 不能放在条件语句中**

##  2 useEffect

![image-20231107231017857](.\images\image-20231107231017857.png)

例子如下

![image-20231107233445272](.\images\image-20231107233445272.png)

##  3 useRef

![image-20231107234039633](.\images\image-20231107234039633.png)

例子如下

![image-20231107234014599](.\images\image-20231107234014599.png)

## 4 useContext 解决多层传值问题

在父组件使用

![image-20231115234010190](.\images\image-20231115234010190.png)

在子组件或后代组件中

![image-20231115234113556](.\images\image-20231115234113556.png)

## 5 useReducer

![image-20231115234840066](.\images\image-20231115234840066.png)

## 6 useReducer和useContext的结合使用代替redux

![image-20231116000106356](.\images\image-20231116000106356.png)



![image-20231116000341645](.\images\image-20231116000341645.png)

![image-20231116000415337](.\images\image-20231116000415337.png)

![image-20231116000430782](.\images\image-20231116000430782.png)

![image-20231116000454614](.\images\image-20231116000454614.png)

![image-20231116000600795](.\images\image-20231116000600795.png)

## 7 useMemo优化React Hooks程序性能

![image-20231116001515621](.\images\image-20231116001515621.png)

![image-20231116001527344](.\images\image-20231116001527344.png)

解决如下

![image-20231116001556942](.\images\image-20231116001556942.png)

##  8 自定义hooks函数

![image-20231116003037001](.\images\image-20231116003037001.png)

![image-20231116003048377](.\images\image-20231116003048377.png)

## 9 useSelector和useDispatch

![image-20231207000833589](.\images\image-20231207000833589.png)

**使用useSelector获取store中的数据 使用useDispatch修改仓库数据** 

修改优化成如下

![image-20231207000229135](.\images\image-20231207000229135.png)

![image-20231207215056218](.\images\image-20231207215056218.png)

优化reducer如下

![image-20231207222435549](.\images\image-20231207222435549.png)

优化模块化数据如下

![image-20231207222733412](.\images\image-20231207222733412.png)

**使得最终的用法类似vuex**

![image-20231207223711297](.\images\image-20231207223711297.png)
