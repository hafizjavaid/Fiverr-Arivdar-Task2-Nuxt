<template>
  <div class="sigin_form">
    <form action="" class="main_form">
      <h1 class="form_title">Register</h1>
      <!-- Input -->
      <div class="s_input">
        <input type="text" class="w50" placeholder="First Name" required />
        <input type="text" class="w50" placeholder="Last Name" required />
      </div>
      <!-- Input -->

       <!-- Input -->
      <div class="s_input">
        <input type="email" class="w100" placeholder="Email" required />
      </div>
      <!-- Input -->


       <!-- Input -->
      <div class="s_input">
        <input type="password" class="w100" placeholder="Password" required />
      </div>
      <!-- Input -->


       <!-- Input -->
      <div class="s_input">
        <input type="text" class="w100" placeholder="Address" required />
      </div>
      <!-- Input -->


 <!-- Input -->
      <div class="s_input">
        <input type="text" class="w33" placeholder="Street" required />
        <input type="text" class="w33" placeholder="House No#" required />
         <input type="text" class="w33" placeholder="City" required />
      </div>
      <!-- Input -->
 <!-- Input -->
      <div class="s_input">
        <input type="text" class="w50" placeholder="Capital" required />
        <input type="text" class="w50" placeholder="Province" required />
      </div>
      <!-- Input -->
      <!-- Login Button -->
      <button type="submit" class="login_btn">Register</button>
      <!-- Login Button -->

      <p>Already have an account? <router-link to="/signin">Login</router-link></p>
    </form>
  </div>
</template>

<script>
export default {
  components: {},
  methods: {
    showPopup() {
      this.show = !this.show;
    },
  },
  data() {
    return {
      show: false,
    };
  },
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
    padding-top: 5px;
    h1 {
      text-align: center;
      font-style: normal;
      font-weight: normal;
      font-size: 56px;
      color: #000000;
      margin: 0;
    }
    .s_input {
      display: flex;
      max-width: 550px;
      width: 100%;
      justify-content: space-between;
    
      flex-wrap: wrap;
    }
    .w50 {
      flex: 0 0 48%;
      max-width: 48%;

      @media(max-width: 560px)
      {
      flex: 0 0 100%;
      max-width: 100%;
    
      }
    }
    .w100 {
      flex: 0 0 100%;
      max-width: 100%;
    }
    .w33{
        flex: 0 0 31%;
      max-width: 31%;
       @media(max-width: 560px)
      {
      flex: 0 0 100%;
      max-width: 100%;
       
      }
    }
    input {
      //   max-width: 550px;

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
      &:focus {
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
      transition: 0.3s linear;
      font-weight: bold;
      cursor: pointer;
      &:focus {
        border: none;
        outline: none;
      }
      &:hover {
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
      margin-bottom: 5px;
      a {
        color: #108cff;
        text-decoration-color: #108cff;
      }
    }
  }
}
</style>
