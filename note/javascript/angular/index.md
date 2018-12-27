# Angular

## angular命令

### 安装angular-cli

```bash
npm install -g @angular/cli
```

**new命令**

```bash
# 新建一个叫project-name的项目
ng new project-name
```

**serve命令**

ng serve 命令会自动开发服务器，并监视你的文件变化，当你修改这些文件时，它就会重新构建应用。

```bash
ng serve --open
## --open参数表示打开浏览器
```

**generate命令**

```bash
# 创建一个名叫app-routing的模块
# --flat 把这个文件放进了 src/app 中，而不是单独的目录中。
# --module=app 告诉 CLI 把它注册到 AppModule 的 imports 数组中。
ng generate module app-routing --flat --module=app

# 创建一个叫heroes的组件
ng generate component heroes

# 创建一个叫hero的服务
ng generate service hero
```

## 重要概念

* 模块：Module
* 组件：Component
* 服务：Service
* 路由：Routing



