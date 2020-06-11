<template>
  <div class="main" v-show="isshow">
    <!-- <van-nav-bar title="用户登录" /> -->
    <van-row type="flex" justify="center" class="line">
      <van-col span="3">&nbsp</van-col>
      <van-col span="18">
        <van-cell-group>
          <van-field placeholder="请输入用户名" type="text" v-model="user" left-icon="manager" />
        </van-cell-group>
        <van-cell-group>
          <van-field placeholder="请输入密码" type="password" v-model="password" left-icon="lock" />
        </van-cell-group>
      </van-col>
      <van-col span="3">&nbsp</van-col>
    </van-row>

    <van-row type="flex" justify="center" class="btns">
      <van-col span="3">&nbsp</van-col>
      <van-col span="18">
        <van-button class="jumpBtn" type="primary" @click="signIn" size="large">登录</van-button>
      </van-col>
      <van-col span="3">&nbsp</van-col>
    </van-row>
  </div>
</template>

<script>
import Vue from "vue";
import axios from "axios"
import { Button, NavBar,Field, Col, CellGroup,Row } from "vant";

// Vue.use(Button)
// Vue.use(Vant)

export default {
  components: {
    [Button.name]: Button,
    [NavBar.name]: NavBar,
    [Field.name]: Field,
    [Col.name]:Col,
    [Row.name]:Row,
    [CellGroup.name]:CellGroup
  },
  data(){
    return{
      user:'liujishu',
      password:'123456',
      isshow:'true'
    }
  },
  methods:{
    signIn:function () {
      console.log(this.user,this.password)
      if (this.user=="liujishu" && this.password=="123456"){
        this.isshow=false
      }
    }
  }
};
</script>

<style scoped>
</style>

