<template>
  <div class="login">
    
      <img src="./../assets/images/bj.jpg" alt="我飘走了">
    
    <div class="login-content">
      <van-cell-group class="kuang">
        <van-field label="用户名" v-model="form.username" placeholder="请输入用户名" />
         <van-divider />
      </van-cell-group>
      <van-cell-group class="kuang">
        <van-field clear="xiahuaxian" label="密码" v-model="form.password" type="password" placeholder="请输入密码" />
       <van-divider />
      </van-cell-group>
     
    </div>
   
    <div class="login-submit">
      <van-button size="default" color="linear-gradient(to right, #4bb0ff, #6149f6)" round style="width:80%" @click="submitHandler">登录</van-button>
    </div>
    <div class="wangji"><a href="#">忘记密码？</a></div>
    <div class="kong"></div>
    
    <div class="xiabu">第三方登录方式 </div>
    <div class="tupian2"><img class="sanfang" src="./../assets/images/dl.jpg" alt=""></div>
     <div class="xiabu">立即注册 </div>
  </div>
</template>
<script>
import {mapState,mapActions} from 'vuex'
export default {
  data(){
    return {
      form:{
        type:"waiter"
      }
    }
  },
  methods:{
    ...mapActions("user",["login"]),
    submitHandler(){
      this.login(this.form)
      .then(()=>{
        this.$router.push("/home")
      })
    }
  }
}
</script>
<style scoped>
.tupian2{
  width: 70%;
  height: 70px;
  text-align: center;
  margin-left: 100px;
  margin-bottom: 20px;

}
img{
  width: 100%;
  height: 50%;
  overflow: hidden;
  margin-bottom: 10px;
}
.wangji{
  width: 30%;
  height: 50px;
  position: absolute;
  right: 0px;
  font-size: 14px import;
}
a{
  /* position:relative; */
  right: 20px;
  font-size: 16px;
  /* margin-right: 20px; */
  right:20px;
  margin-top:20px;
  line-height: 50px;
  margin-left:50px;
  
}
.xiahuaxian{
  border-bottom: 1px solid ;
}

.login-content {
  margin-bottom: 1em;
  
}
.sanfang{
  margin-top: 20px;
  width: 70%;
  height: 50px; 
  /* display: inline-block; */
 /* /* text-align: center; */
}
.kong{
  width: 100%;
  height: 250px;
}
.kuang{
  /* width: 80%; */
  height: 80px;
  font-size: 20px;
}
.login-submit {
  text-align: center;
  margin-top: 40px;
  width: 60%;
  height: 50px;
  font-size: 20px;
  margin:0 auto;
}
.xiabu{
  /* position: absolute;
  bottom:265px;
  left: 165px; */
  /* display:inline-block; */
  text-align: center;
  margin: 0 auto;
  font-size: 20px;
  color: #5875a4;

  
}
.xiabu2{
  position: absolute;
  bottom:100px;
  left: 200px;
  /* margin:0 auto; */
  font-size: 20px;
  color: #5875a4;

  
}
.xia1{
  display:inline-block;
  margin-right: 20px;
  width: 100px;
  height: 50px;
  font-size: 20px;
  text-align: center;
  color: #5875a4;

}
</style>