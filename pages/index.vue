<template>
  <div class="sigin_form">
    <form action="" class="main_form">
      <h1 class="form_title">Sign In</h1>
      <!-- Input -->
      <input type="text" placeholder="Email" required />
      <!-- Input -->
      <!-- Input -->
      <input type="password" placeholder="Password" required />
      <!-- Input -->

      <!-- Login Button -->
      <button type="submit" class="login_btn">Login</button>
      <!-- Login Button -->
      <a href="#" class="f_password" @click="showPopup">Forgot Password?</a>
      <p>Don’t have an account? <router-link to="/register">Register</router-link></p>
    </form>
    <Popup v-if="show" @close="close"></Popup>
  </div>
</template>

<script>
import Popup from "@/components/Confirmpassword";
export default {
    name:"Signin",
  components: {
    Popup,
  },
  methods:{
    showPopup(){
this.show = !this.show;
    },
     close(){
this.show = !this.show;
    }
  },
  data(){
    return{
      show:false
    }
  }
};
</script>

<style lang="scss" scoped>
.sigin_form {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  .main_form {
    max-width: 600px;
    width: 100%;
    margin: auto;
    padding: 20px;
    h1 {
      text-align: center;
      font-style: normal;
      font-weight: normal;
      font-size: 56px;
      color: #000000;
      margin: 0;
    }
    input {
      max-width: 550px;
      width: 100%;
      height: 45px;
      border: 1px solid #000000;
      margin-top: 25px;
      padding: 15px;
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      line-height: 19px;
      color: #000000;
      background: transparent !important;
      &:focus{
        border: 2px solid #000;
        outline: none;
      }
    }
    .login_btn {
      max-width: 550px;
      width: 100%;
      height: 45px;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #000000;
      border: 1px solid #ffffff;
      color: #ffffff;
      margin-top: 25px;
      transition: .3s linear;
      font-weight: bold;
       cursor: pointer;
      &:focus {
        border: none;
        outline: none;
      }
      &:hover{
        background-color: #ffffff;
        color: #000;
        font-weight: bold;
        border: 1px solid #000;
      }
    }
    .f_password {
      text-align: center;
      width: 100%;
      display: inline-block;
      margin-top: 11px;

      color: #108cff;
      text-decoration-color: #108cff;
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
    }
    p {
      font-style: normal;
      font-weight: normal;
      font-size: 16px;
      margin-top: 18px;
      a {
        color: #108cff;
        text-decoration-color: #108cff;
      }
    }
  }
}
</style>
