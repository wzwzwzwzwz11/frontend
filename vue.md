# setup

- 在 beforeCreate() 钩子之前，自动执行
- 语法糖 `<script setup>`
- setup中 this不指向组件实例，指向undefined

# ref & reactive

- 作用：用函数调用的方式生成响应式数据
- 区别：
  - reactive:只能处理对象类型，不能处理简单类型
  - ref：可以处理包括对象类型和简单类型的数据，通过.value获取值
  - ref函数的内部实现依赖于reactive
- 推荐使用 ref

# computed计算属性

- 计算属性不应该有副作用：比如异步请求，修改dom
- 避免直接修改计算属性的值：计算属性应该是只读