// 代码实现
<template>
    <div>
        <!-- 动态绑定class
  				v-bind:class = '{类名: 布尔值}'
   				:class="{类名: 布尔值}"
     		 	使用场景: vue变量控制标签是否应该有类名-->

        <p v-bind:class="{'active': activeFlag}">我是p标签</p>
        <button @click="activeFlag = !activeFlag">
            Click me
        </button>
        <!-- v-bind:class指令可以与普通的class特性共存 -->
        <div class="box" :class="{'active': activeFlag}">
          我是div
        </div>
    </div>
</template>

data() {
  return {
    activeFlag: true
  };
},
