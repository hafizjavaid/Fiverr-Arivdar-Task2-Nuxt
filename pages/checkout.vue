<template>
  <div class="sigin_form">
    <form action="" class="main_form">
      <h1 class="form_title">Checkout</h1>
      <!-- Input -->
      <div class="s_input">
        <div class="w50 data" >Hafiz</div>
         <div  class="w50 data">Javaid Iqbal</div>
      </div>
      <!-- Input -->

       <!-- Input -->
      <div class="s_input">
        <div  class="w100 data">30$</div>
      </div>
      <!-- Input -->

 <!-- Input -->
      <div class="s_input">
        <input type="text" class="w33" placeholder="Card Number" required />
        <input type="date" class="w33" placeholder="Expire Date" required />
         <input type="text" class="w33" placeholder="CVV Number" required />
      </div>
      <!-- Input -->
      <!-- Login Button -->
      <button type="submit" class="login_btn">Checkout</button>
      <!-- Login Button -->
    </form>
  </div>
</template>

<script>
export default {
  components: {},
  methods: {
   
  },
  data() {
    return {
     
    
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
    border: 2px solid red;
    @media(max-width:560px)
    {
      width: 95%;
    }
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
        flex: 0 0 32%;
      max-width: 32%;
       @media(max-width: 560px)
      {
      flex: 0 0 100%;
      max-width: 100%;
       
      }
    }
    .data{
    
       width: 100%;
      height: 45px;
      border-bottom: 2px solid red;
      margin-top: 25px;
      font-style: normal;
      font-weight: bold;
      font-size: 16px;
      line-height: 19px;
      color: #000000;
      display: flex;
      justify-content: center;
      align-items: center;
 
    }
    input {
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
      background-color: red;
      margin-top: 25px;
      transition: 0.3s linear;
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
        border: 1px solid red;
      }
    }
    
  }
}
</style>
