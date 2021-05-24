## 安装依赖
npm install

## 启动React不同版本的调试环境：
* 启动17正式版
```
 npm run dev:17
```

* 查看Lanes优先级模型的效果（除react、react-dom之外，其他包例如 scheduler、react-reconciler等引入自master分支的代码）

*在此感谢[yisar](https://github.com/yisar)提供Lanes模型的源码包*

由于Lanes还未正式发布，master分支代码虽然开启concurrent模式之后优先级用的就是lanes，但它只是将expirationTime替换成了lanes去实现，
效果并无变化，真正的效果可以使用下边命令预览，启动命令之前需要将config/env.js 中的__PROFILE__环境变量置为true
```
npm run dev:lanes
```