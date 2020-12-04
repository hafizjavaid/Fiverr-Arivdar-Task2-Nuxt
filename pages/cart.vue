<template>
  <section class="cart_section">
    <div class="cart_inner">
        <h1 class="title">Product Cart</h1>
      <div class="cart_header">
        <h1 class="product">Product</h1>
        <h1 class="price">Price</h1>
        <h1 class="quantity">Quantity</h1>
        <h1 class="t_price">Total Price</h1>
      </div>
      <div class="main_item" v-for="(product,i) in Products" :key="i">
        <div class="m_product">
          <img :src="product.img" alt="" />
          <div class="p_detail">
            <h1>{{product.title}}</h1>
            <p>
                <span>{{product.variations[0]}}</span> - 
                <span>{{product.variations[1]}}</span>
            </p>
          </div>
        </div>
        <h3 class="m_price"><span>Price :</span>{{product.price}}$</h3>
        <div class="m_quantity">
          <div class="boxes">
            <div class="add box" @click="add(i)">+</div>
            <div class="content">{{product.count}}

            </div>
            <div class="sub box" @click="sub(i)">-</div>
          </div>
          <div class="remove_icon" @click="remove(i)">
             <font-awesome-icon :icon="['fas', 'trash']"/>
          
          </div>
        </div>
        <h3 class="m_tprice"><span>Total Price :</span>{{(product.price)*(product.count)}}$</h3>
          <div class="remove_icon_2" @click="remove(i)">
             <font-awesome-icon :icon="['fas', 'trash']"/>
          
          </div>
      </div>
     
     <!-- CheckOut Form -->
     <form action="" class="main_form">
     
     <div class="t_checkbox">
          <input type="text" placeholder="Delivery Address" required />
      <div class="checkbox">
        <input type="checkbox" id="toggle" v-model="checked">
        <label for="toggle">Billing Address is same as Delivery Address</label>
      </div>
     
     </div>
      
    
      <!-- Input -->
      <input type="text" v-if="!checked" placeholder="Billing Address" required />
      <!-- Input -->
      <!-- CheckBox -->
     
     
     <!-- CheckBox -->
      <!-- Login Button -->
      <router-link to="/checkout" class="login_btn">CheckOut</router-link>
      <!-- Login Button -->
     
    </form>
     <!-- CheckOut Form -->

    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      Products: [
        {
          id: 1,
          title: "Google Pixel",
          variations: ["Black", "2GB Size"],
          img: require(`~/assets/images/1.jpg`),
          price: 10,
          count: 1,
          total: 0,
        },
        {
          id: 2,
          title: "Google Pixel",
          variations: ["Black", "2GB Size"],
          img: require(`~/assets/images/2.jpg`),
          price: 10,
          count: 1,
          total: 0,
        },
        {
          id: 3,
          title: "Google Pixel",
          variations: ["Black", "2GB Size"],
          img: require(`~/assets/images/3.jpg`),
          price: 10,
          count: 1,
          total: 0,
        },
      ],
      checked:true
    };
  },
  methods:{
      add(i){
         this.Products[i].count += 1;
         
      },
       sub(i){
         this.Products[i].count -= 1;
         if(this.Products[i].count == 0)
         {
            this.remove(i);
         }
         
      },
      remove(i){
          this.Products.splice(i,1);
      }
      
  }
};
</script>


<style lang="scss" scoped>
.cart_section {
  display: flex;
  justify-content: center;
  align-items: center;
//   height: 100vh;
 font-family: 'Nunito', sans-serif;

  background-color: #eee;

  .cart_inner {
    max-width: 1100px;
    margin: auto;
    width: 100%;
    padding: 10px;
    padding: 20px 5px;
    .title{
        text-align: center;
        margin-bottom: 30px;
        font-size: 40px;
    }
    .cart_header {
      display: flex;
      justify-content: space-between;
      max-width: 100%;
      width: 100%;
      margin-bottom: 20px;
      @media (max-width: 580px) {
        display: none;
      }
      .product {
        flex: 0 0 38%;
        max-width: 38%;
      }
      .quantity {
        flex: 0 0 28%;
        max-width: 28%;
      }
      .price {
        flex: 0 0 15%;
        max-width: 15%;
      }
      .t_price {
        flex: 0 0 15%;
        max-width: 15%;
        text-align: center;
      }
      h1 {
        text-align: left;
      }
    }
    .main_item {
      display: flex;
      justify-content: space-between;
      max-width: 100%;
      width: 100%;
      background: #fff;
      padding: 20px 10px;
      flex-wrap: wrap;
      margin: 20px 0;
      .m_product {
        flex: 0 0 38%;
        max-width: 38%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        @media (max-width: 580px) {
          flex: 0 0 100%;
          max-width: 100%;
          justify-content: center;
        }

        img {
       
          width: 100px;
          height: 100px;
        //   justify-self: start;
       
        }
        .p_detail {
          flex: 0 0 70%;
          max-width: 70%;
           margin: 10px 0;
          @media(max-width:580px)
          {
              flex: 0 0 100%;
              max-width: 100%;
            width: 100%;
            margin: 10px 0;
           
          }
          h1,
          p {
            text-align: left;
            @media(max-width:580px)
          {

            text-align: center;
          }
          }
          h1{
              font-size: 20px;
               font-weight: 500;
          }
          p{
              font-size: 16px;
          }
        }
      }
      .m_price {
        flex: 0 0 15%;
        max-width: 15%;
        display: flex;
        align-items: center;
          span {
          display: none;
        
        }
        @media (max-width: 580px) {
          flex: 0 0 100%;
          max-width: 100%;
          span{
              display: inline-block;
          }
          justify-content: center;
          margin: 15px 0;
        }
       
      }
      .m_quantity {
        flex: 0 0 28%;
        max-width: 28%;
        display: flex;
        justify-content: space-between;
        width: 100%;
        align-items: center;
        @media (max-width: 580px) {
          flex: 0 0 100%;
          max-width: 100%;
          margin: 15px 0;
        }
        .boxes {
          display: flex;
          flex: 0 0 80%;
          max-width: 80%;
           @media(max-width:580px)
            {
                justify-content: center;
                flex: 0 0 100%;
    max-width: 100%;
            }
          .box
          {
            width: 30px;
            height: 30px;
            border: 2px solid #000;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 5px;
            cursor: pointer;
            transition: .3s linear;
            &:hover{
                background-color: #000;
                color: #fff;
                // border-color: #fff;
            }
          
           
          }
            .content{
            width: 30px;
            height: 30px;
            border: 2px solid #000;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 5px;
            cursor: pointer;
            transition: .3s linear;
                &:hover{
                    background-color: none !important;
                    color: #000 !important;
                }
            }
        }
        .remove_icon {
          flex: 0 0 18%;
          max-width: 18%;
          justify-self: flex-start;
          transform: translateX(-100%);
          @media(max-width:580px)
          {

          display: none;
          }
          @media (max-width: 767px) {
            transform: translateX(0%);
          }
          svg{
              cursor: pointer;
              color: red;
          }
        }
      }
      .m_tprice {
        flex: 0 0 15%;
        max-width: 15%;
        display: flex;
        align-items: center;
        justify-content: center;
        span {
          display: none;
          @media (max-width: 580px) {
            display: inline-block;
          }
        }
        // text-align: center;
        @media (max-width: 580px) {
          flex: 0 0 100%;
          max-width: 100%;
           margin: 15px 0;
        }
      }
      .remove_icon_2{
          display: none;
          @media(max-width:580px)
          {
              display: flex;
              flex: 0 0 100%;
              justify-content: center;
              max-width: 100%;
          }
          svg{
               color: red;
               cursor: pointer;
          }
      }
    }
     .main_form {
    max-width: 100%;
    width: 100%;
    // margin: auto;
    padding: 20px;
    padding-left: 0;
    .t_checkbox{
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
    .checkbox{
        display: flex;
        align-items: center;
        label{
            margin-top: 25px;
            @media(max-width:470px)
            {
                font-size: 14px;
            }
        }
    }
    }
    input[type="text"] {
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
      &:focus{
        border: 2px solid #000;
        outline: none;
      }
    }
    #toggle{
        margin-top: 25px;
        width: 17px;
        height: 17px;
        cursor: pointer;
        
    }
    label{
        margin-left: 10px;
       
        display: inline-block;
        font-size: 20px;
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
       text-decoration: none;
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
   
  }
  }
}
</style>
