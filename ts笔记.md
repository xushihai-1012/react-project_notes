## Record

**链接：https://juejin.cn/post/7280088532377681961**

### 1. 定义

在 TypeScript 中，泛型工具类型 `Record<K, T>` 主要用于创建一个由给定键类型 K 映射到值类型 T 的新类型。

Record 工具类型有2个类型参数 K 和 T，其中：

- K 表示的是：创建的新对象需要有哪些属性，属性可以只有一个，也可以有多个，多个属性时采用“联合类型”的写法
- T 表示的是：对象属性的类型。

### 2. 源码

```typescript
typescript复制代码type Record<K extends keyof any, T> = {
  [P in K]: T;
};
```

实现原理：

- 上面这段代码中，使用 type 关键字来定义 `Record<K extends keyof any, T>` 类型，它接收两个类型参数 K 和 T。
- 第一个参数 K extends keyof any 表示的是泛型参数 K 必须是一个能作为对象键的类型。
- 然后，使用映射类型的语法 `{ [P in K]: T }` 来创建一个新的类型，这里的 `[P in K]` 表示的是：遍历 K 中的每个键，并将其作为属性名，然后将类型 T 分配给每个属性。
- 整段代码的含义就是：使用 Record 来创建一个新的对象类型，类型将拥有 K 中的每个键，并且每个键对应的属性值类型为 T。

下面我们先看下 Record<K, T> 的基本用法：

```typescript
typescript复制代码type Direction = "up" | "right" | "down" | "left";
type RecordDirection = Record<Direction, number>;

const direction: RecordDirection = {
  up: 1,
  right: 2,
  down: 3,
  left: 4,
};
```

上面这段代码中，RecordDirection 类型被定义为 Record<RecordDirection, number>，它将联合类型 "up" | "right" | "down" | "left"中的每个键作为属性，并将 number 类型作为属性值的类型，生成的 direction 对象需要符合该类型，使用 Record 创建的新类型，等同于下面的这段代码：

```typescript
typescript复制代码type RecordDirection = {
  up: number;
  right: number;
  down: number;
  left: number;
}
```

### 3. 使用场景

#### 3.1. 初始化对象

当你需要创建一个初始值为特定类型的属性的对象时，可以使用 Record。

```typescript
typescript复制代码interface IPerson {
  name: string;
  age: number;
  email: string;
  gender: string;
};

type Person = Record<keyof IPerson, string>

const person: Person = {
  name: "Echo",
  age: "26",
  email: "test@123.com",
  gender: "Male",
};
```

上面这段代码中，我们使用 Record<keyof IPerson, string> 来创建一个新的类型 Person，其中，参数 keyof IPerson 用于获取 IPerson 类型中所有键的关键字，返回类型是联合类型："name" | "age" | "email" | "ender"，然后我们创建了一个名为 person 的对象，类型为 Person，此时，person 对象中必须具备 name、age、email 和 gender 这4个属性，同时我们也可以为每个属性提供默认值。

#### 3.2. 枚举值管理

如果你有一个固定的枚举值列表，并且需要将每个枚举值映射为特定类型的属性，可以使用 Record。

```typescript
typescript复制代码enum Color {
  Red = "RED",
  Green = "GREEN",
  Blue = "BLUE",
}

type ColorHexCode = Record<Color, string>;

const colorHexCode: ColorHexCode = {
  [Color.Red]: "#FF0000",
  [Color.Green]: "#00FF00",
  [Color.Blue]: "#0000FF",
};
```

上面这段代码中，Color 枚举定义了一些颜色常量。通过使用 Record，我们创建了 ColorHexCode 类型，将每个颜色映射为对应的十六进制代码。colorHexCode 对象存储了每个颜色常量与其相应的十六进制代码之间的映射。