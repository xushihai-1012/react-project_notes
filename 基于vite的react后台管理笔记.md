## 一 执行脚手架命令初始化项目

```
pnpm create vite
```



## 二 样式初始化

**执行命令**

```
pnpm install normalize.css 
```

在main.tsx导入 import 'normalize.css'

或者

```
pnpm install reset-css
```

在main.tsx导入 import 'reset-css'

**reset-css初始化更彻底  normalize.css会尽量保留浏览器的默认样式**



## 三 安装scss

**执行命令**

```
pnpm i sass -D
```

**vite 已配置好loader 安装即可**



## 四 配置路径别名

在vite.config.ts文件中

```ts
import path from "path";

export default defineConfig({
  plugins: [react()],
  resolve: {
    alias: {
      "@": path.resolve(__dirname, "./src"),
    },
  }
});
```

**导入path模块会变红 是因为缺少ts的声明 执行如下命令安装就好**

```
pnpm i @types/node -D
```

**配置路径别名提示 在tsconfig.json文件中添加如下**

```json
"compilerOptions": {
    "baseUrl": "./",
    "paths": {
      "@/*": [
        "src/*"
      ]
    },
    .....
}
```



## 五 模块化导入scss

**为了不影响全局的其他模块的css 使用如下方法导入scss 类似vue中的style的scoped**

![image-20231122233332167](.\images\image-20231122233332167.png)



## 六 安装antd

执行如下命令

```
pnpm i antd
```

安装图标组件

```
pnpm i @ant-design/icons
```



## 七 路由配置方案 旧方案

### 1 组件路由方案

![image-20231123222620298](.\images\image-20231123222620298.png)

![image-20231123222637652](.\images\image-20231123222637652.png)

![image-20231123223956621](.\images\image-20231123223956621.png)

 ![image-20231123223814490](.\images\image-20231123223814490.png)



### 2 编程式导航--设置裁断点击跳转

![image-20231123224141196](.\images\image-20231123224141196.png)  



## 八 路由配置方案 新方案

### 1 对象方案

![image-20231123225206675](.\images\image-20231123225206675.png)

![image-20231123225511044](.\images\image-20231123225511044.png)

![image-20231123225324033](.\images\image-20231123225324033.png)



### 2 路由懒加载

![image-20231123225728164](.\images\image-20231123225728164.png)

![image-20231123230052716](.\images\image-20231123230052716.png)

![image-20231123230020314](.\images\image-20231123230020314.png)

### 3 路由懒加载简写方式

![image-20231123230343383](.\images\image-20231123230343383.png)

## 九 解决ts报错问题

![image-20231202222102435](.\images\image-20231202222102435.png)



