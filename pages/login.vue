<template>
  <div class="box">
    <div class="login_content">
      <!-- logo图标 -->
      <div class="logo">
        <div class="qq">
          <img class="logo_img" src="@/static/assets/img/100.jpg" alt="" />
          <div>222</div>
        </div>
      </div>
      <!-- 手机号 -->
      <div class="user_login">
        <div class="phone_num">
          <van-cell-group>
            <van-field v-model="phone" type="tel" placeholder="请输入手机号" />
          </van-cell-group>
        </div>

        <div class="verification_code">
          <van-cell-group >
            <van-field
              v-model="value" placeholder="请输入验证码"
            />
          </van-cell-group>
          <div class="buts">
            3333
          </div>
        </div>
      </div>
      <!-- 登录 -->
      <div class="but"></div>
    </div>
    <!-- <button :style="youzhi? '#ccc':'#000'" @click="qq"></button> -->
  </div>
</template>

<script>
import { Field, CellGroup } from 'vant'
export default {
  name: 'LoginPage',
  head: {
    title: '登录',
  },
  components: {
    [Field.name]: Field,
    [CellGroup.name]: CellGroup,
  },
  data() {
    return {
      phone: '',
    }
  },
  mounted() {},
  methods: {},
}
</script>
<style lang="scss" scoped>
.box {
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow: hidden;
  background: rgb(204, 192, 192);
  .login_content {
    width: 100%;
    .logo {
      width: 100%;
      height: 30vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background: rgb(224, 243, 206);
      .qq {
        // width: 50px;
        display: flex;
        flex-direction: column;
        align-items: center;
        .logo_img {
          width: 200px;
          height: 200px;
        }
      }
    }
    .user_login {
      width: 100%;

      .phone_num{
        margin: 0 auto;
        width: 93%;
      }
      .verification_code {
        margin: 0 auto;
        width: 93%;
        display: flex;
        .buts{
          flex: 1;
          
          background: aqua;
        }
      }
    }

    .but {
    }
  }
}


 
</style>
