# less

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


### conslusion
1. 坑啊，用less.modifyVar方法，必须要在header中挂在需要用的样式
2. 不能在每个单独的文件中定义变量样式，也就是说提前在header中引入的样式，包含好你想动态改变的样式
3. 坑啊，ant-design-vue组件库也一样，自己项目中也要把想定义的class类名预先准备一份
4. 坑啊，我一直认为很高深呢，没想到啊，坑了我一下午！！！
