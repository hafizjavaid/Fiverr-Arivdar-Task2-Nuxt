<template>
  <div class="p_modal">
    <div class="main_modal">
      <h1>Recover Password</h1>
      <p>You will receive a recovery email at this email</p>
      <form action="">
        <!-- Input -->
        <input type="email" placeholder="Email" required />
        <!-- Input -->
         <!-- Login Button -->
      <button type="submit" class="submit_btn" @click="submit">Submit</button>
       <!-- Login Button -->
        <p>Didn’t received? <a @click="resend">Resend</a></p>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  methods:{
    submit(){
      this.$emit("close");
    },
    resend(){
      this.$emit("close");
    }
  }
};
</script>

<style lang="scss" scoped>
.p_modal {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: "Roboto", sans-serif;
  z-index: 9;
  background-color: rgba(0,0,0,0.5);
 

  .main_modal {
    max-width: 581px;
    background-color: #fff;
   
    margin: auto;
  
    width: 94%;
    min-height: 350px;
   
    padding: 20px;
    padding-top: 25px;
    h1,
    p {
      text-align: center;
    }
    form {
      max-width: 450px;
      margin: auto;
      width: 100%;

      input {
        max-width: 441px;
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
         &:focus{
        border: 2px solid #000;
        outline: none;
      }
      }
          .submit_btn{
      max-width: 441px;
      width: 100%;
      height: 45px;
        display: flex;
  justify-content: center;
  align-items: center;
  background: #000000;
border: 1px solid #FFFFFF;
color: #FFFFFF;
background-color: red;
 margin-top: 25px;
 transition: .3s linear;
 font-weight: bold;
 cursor: pointer;

&:focus{
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
  p{
        font-style: normal;
font-weight: normal;
font-size: 16px;
 margin-top: 18px;
 text-align: left;
a{

        color: #108CFF;
        text-decoration-color:#108CFF;
        cursor: pointer;
}}
    }
  }
}
</style>
