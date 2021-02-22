<!--  -->
<template>
  <tab-bar>
    <tab-bar-item path="/home" >
      <!-- 通过具名插槽动态的来决定每一个图片，每一个文字 -->
      <!-- 可以插入多个3个5个6个等等，不用再考虑样式等问题 -->
      <img slot="item-icon" src="~assets/img/tabbar/iconfont-home.png" alt="">
      <img slot="item-icon-active" src="~assets/img/tabbar/iconfont-home1.png" alt="">
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category" >
      <img slot="item-icon" src="~assets/img/tabbar/iconfont-31leimu.png" alt="">
       <img slot="item-icon-active" src="~assets/img/tabbar/iconfont-31leimu1.png" alt="">
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart">
      <img slot="item-icon" src="~assets/img/tabbar/iconfont-cart.png" alt="">
       <img slot="item-icon-active" src="~assets/img/tabbar/iconfont-cart1.png" alt="">
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="profile">
      <img slot="item-icon" src="~assets/img/tabbar/iconfont-people.png" alt="">
       <img slot="item-icon-active" src="~assets/img/tabbar/iconfont-people1.png" alt="">
      <div slot="item-text">我的</div>
    </tab-bar-item>
  </tab-bar>

</template>

<script>
import TabBar from 'components/common/tabbar/TabBar.vue'
import TabBarItem from 'components/common/tabbar/TabBarItem.vue'
export default {
  name:'MainTabBar',
  components:{
    TabBar,
    TabBarItem
  },
  data () {
    return {
    };
  },
}

</script>
<style scoped>
</style>
