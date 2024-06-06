# study markdown

## 1. 初始化

### 1.1 构造函数 `Vue`

这里定义了`Vue`的构造函数，通过一系列函数调用, 扩展其原型上的属性和方法
```ts
function Vue(options) {
  this._init(options)
}
initMixin(Vue)
stateMixin(Vue)
eventsMixin(Vue)
lifecycleMixin(Vue)
renderMixin(Vue)
```
### 1.1 initMixin

```ts
export function initMixin(Vue: Class<Component>) {
  Vue.prototype._init = function (options?: Object) {
  //  ...
  }
}
```
**initMixin** 主要是给 Vue.prototype._init 赋值，这个方法在实例化 Vue 的时候会被调用 


使用with会触发 Proxy 中的 has