<template>
  <div>
    <!-- 2.过滤器的使用
      1. 在插值表达式 和  v-bind的表达式里可以用
      {{ message | 过滤器的名称 }}
      实现一个把所有字母转换成大写的过滤器
     -->
     <p>原来的样子： {{msg}}</p>
     <p>使用翻转过滤器：{{msg | reverse}}</p>
     <p :title="msg | toUp">鼠标常停</p>
      
  </div>
</template>

<script>
export default {
  data(){
    return {
      msg: 'Hello, Vue'
    }
  },
  // 方式2: 局部 - 过滤器
  // 只能在当前vue文件内使用
  /*
     语法: 
     filters: {
       过滤器名字 (val) {
         return 处理后的值
       }
     }
  */
  filters: {
    toUp (val) {
      return val.toUpperCase()
    }
  }
}

</script>