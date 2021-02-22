<!--  -->
<template>
  <div class="nav-bar">
    <div class="left"><slot name="left"></slot></div>
    <div class="center"><slot name="center"></slot></div>
    <div class="right"><slot name="right"></slot></div>
  </div>
</template>

<script>
export default {
  name:'Navbar',
  data () {
    return {
    };
  },
}

</script>
<style scoped>
  .nav-bar{
    display: flex;
    height: 44px;
    /* 导航栏一般是44，如果加上状态栏的话会是64 */
    line-height: 44px;
    text-align: center;
    /* 导航条阴影 */
    box-shadow: 0 1px 1px rgba(100, 100, 100, 0.1);
  }
  .left, .right{
    width: 60px;
    /* background-color: #42B983; */
  }
  .center{
    flex: 1;
    /* background-color: #2C3E50; */
  }
</style>
