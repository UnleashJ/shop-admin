## 代码格式化配置

### ESLint初始配置

vite创建的项目默认没有集成ESLint，我们参照ESLint[官网](https://eslint.org/docs/latest/user-guide/getting-started)安装配置ESLint，并在脚本命令中添加lint：

```json
"scripts": {
    "dev": "vite",
    "build": "vue-tsc --noEmit && vite build",
    "preview": "vite preview",
    "lint": "eslint ./src/**/*.{js,jsx,vue,ts,tsx} --fix"
  },
```

Vue3中，模板可以不必须有唯一根节点。ESLint中仍然使用Vue2的模板校验规则，需要修改ESLint配置文件

```js
extends: [
    'plugin:vue/essential',
    'standard'
],
```

修改为

```js
extends: [
    'plugin:vue/vue3-strongly-recommended',
    'standard'
],
```

### 编辑器集成

1. 禁用Vetur插件
2. 安装ESLint插件
3. 安装Volar插件



### git commit hook

在进行git提交操作时，执行的钩子函数（可以自动执行lint命令）。

```
npx mrm@2 lint-staged
```

