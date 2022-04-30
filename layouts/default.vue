<template>
  <div class="box">
    <div class="topBar">
      <div class="icon">
        <van-icon name="home-o" />
      </div>
      <div class="txt">{{ title }}</div>
    </div>
    <div class="content">
      <transition :name="transitionName" mode="in-out">
        <nuxt />
      </transition>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      title: '骆驼门店仓库管理',
      transitionName: 'slide-forward'
    }
  },
  watch: {
    $route(to, from) {
      // if (this.transitionName !== 'slide-forward') {
      //   this.transitionName = 'slide-forward'
      // } else {
      //   this.transitionName = 'slide-back'
      // }
      // console.log('路由变化')
      // console.log(to, from)
    },
  },
  mounted() {
    console.log(this.$router.currentRoute)
  },
}
</script>

<style lang="scss" scoped>
.box {
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
  overflow: hidden;
}

.topBar {
  width: 100%;
  height: 80px;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  position: relative;
  .txt {
    flex: 1;
    text-align: center;
    font-size: 26px;
  }
  .icon {
    border-radius: 50%;
    border: 1px solid #333;
    width: 30px;
    height: 30px;
    margin: 0 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 16px;
  }
}

.content {
  flex: 1;
  overflow: hidden;
  overflow-y: auto;
}
</style>
