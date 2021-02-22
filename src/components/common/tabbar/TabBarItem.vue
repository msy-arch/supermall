<!--  -->
<template>

  <div class="tab-bar-item" @click="itemClick()">
    <!-- 通过具名插槽来动态展示 -->
    <!-- 给slot外面包装一个div,以免slot出现什么错误 -->
    <div v-if="!isActive"><slot name="item-icon"></slot></div>
    <div v-else><slot name="item-icon-active"></slot></div>
    <!-- <div :class="{active:isActive}"> <slot name="item-text"></slot></div> -->
    <div :style="activeStyle"> <slot name="item-text"></slot></div>

    <!-- 所有的item都展示同一个图片，同一个文字 -->
    <!-- 不能写死 -->
    <!-- <img src="../../assets/img/tabbar/iconfont-home.png" alt="">
    <div>首页</div> -->
  </div>

</template>

<script>
export default {
  name:'TabBarItem',
  props:{
    path:String,
    activeColor:{
      type:String,
      default:'#d4237a'
    }
  },
  data () {
    return {
      // isActive:true,
    };
  },
  computed:{
    isActive() {
      // 当前活跃的路由是否和props传来的一样
      //  /home -> item1(/home) = true
      //  /home -> item2(/category) = false
      //  /home -> item3(/cart) = false
      //  /home -> item4(/profile) = false
      return this.$route.path.indexOf(this.path) !== -1
    },
    activeStyle() {
      return this.isActive ? {color:this.activeColor} : {}
    }
  },
  methods:{
    itemClick() {
      this.$router.replace(this.path)/* .catch(() => {}) */
    }
  }

}

</script>
<style scoped>
  .tab-bar-item{
    flex: 1;
    text-align: center;
    height: 49px;
    font-size: 14px;

  }
  .tab-bar-item img{
    height: 24px;
    width: 24px;
    margin-top: 3px;
    vertical-align: middle;
    margin-bottom: 2px;
  }
  /* .active{
    color: #d4237a;
  } */
</style>
