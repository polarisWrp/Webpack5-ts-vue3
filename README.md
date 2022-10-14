## 本项目构建
---
- webpack5,typescript,Vue3,pinia,VueRouter4
- tailwind
- eslint,prettier,husky
- node16.17.0
---

## husky 代码提交动作（commit）的时候自动运行代码校验
```bash
npm run prepare  //生成 .husky文件
npx husky add .husky/pre-commit "npx lint-staged"  // 会在 .husky 目录下自动生成一个 pre-commit 文件
```

## webpack设置路径别名
- 文件使用时找不到声明
- 在tsconfig.json 中添加
```
"baseUrl": "./",                                 
"paths": {
  "@/*": ["src/*"]
},  
```

## eslint关闭未声明变量报错
```
'@typescript-eslint/no-unused-vars': ['warn'],
'no-unused-vars': 'warn',
```
```
webpack5-ts-vue3
├─ .eslintignore
├─ .eslintrc.js
├─ .git
│  ├─ config
│  ├─ description
│  ├─ FETCH_HEAD
│  ├─ HEAD
│  ├─ hooks
│  │  ├─ applypatch-msg.sample
│  │  ├─ commit-msg.sample
│  │  ├─ fsmonitor-watchman.sample
│  │  ├─ post-update.sample
│  │  ├─ pre-applypatch.sample
│  │  ├─ pre-commit.sample
│  │  ├─ pre-push.sample
│  │  ├─ pre-rebase.sample
│  │  ├─ pre-receive.sample
│  │  ├─ prepare-commit-msg.sample
│  │  └─ update.sample
│  ├─ info
│  │  └─ exclude
│  ├─ objects
│  │  ├─ info
│  │  └─ pack
│  └─ refs
│     ├─ heads
│     └─ tags
├─ .gitignore
├─ .husky
│  ├─ pre-commit
│  └─ _
│     ├─ .gitignore
│     └─ husky.sh
├─ auto-imports.d.ts
├─ babel.config.js
├─ components.d.ts
├─ config
│  ├─ webpack.base.js
│  ├─ webpack.dev.js
│  └─ webpack.prod.js
├─ dist
│  ├─ css
│  │  └─ main.3cec8fb38c0da2ef88d9.css
│  ├─ index.html
│  ├─ js
│  │  └─ main.3cec8fb38c.js
│  └─ public
│     ├─ index.html
│     └─ xxx.js
├─ lint-staged.config.js
├─ package-lock.json
├─ package.json
├─ postcss.config.js
├─ public
│  ├─ index.html
│  └─ xxx.js
├─ README.md
├─ src
│  ├─ App.vue
│  ├─ assets
│  │  └─ styles
│  │     ├─ common.scss
│  │     ├─ mixins.scss
│  │     └─ tailwind.css
│  ├─ components
│  │  ├─ login.vue
│  │  └─ reg.vue
│  ├─ main.ts
│  ├─ router
│  │  └─ index.ts
│  ├─ shims-vue.d.ts
│  ├─ store
│  │  └─ index.ts
│  └─ typings.d.ts
├─ tailwind.config.js
└─ tsconfig.json

```
