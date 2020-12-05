<template>
  <section class="cart_section">
    <!-- Cart -->
    <div class="cart_inner">
      <h1 class="title">Product Cart</h1>
      <div class="cart_header">
        <h1 class="product">Product</h1>
        <h1 class="price">Price</h1>
        <h1 class="quantity">Quantity</h1>
        <h1 class="t_price">Total Price</h1>
      </div>
      <!-- Single Item -->
      <div class="main_item" v-for="(product, i) in Products" :key="i">
        <div class="m_product">
          <img :src="product.img" alt="" />
          <div class="p_detail">
            <h1>{{ product.title }}</h1>
            <p>
              <span>{{ product.variations[0] }}</span> -
              <span>{{ product.variations[1] }}</span>
            </p>
          </div>
        </div>
        <h3 class="m_price"><span>Price :</span>{{ product.price }}$</h3>
        <div class="m_quantity">
          <div class="boxes">
            <div class="add box" @click="add(i)">+</div>
            <div class="content">{{ product.count }}</div>
            <div class="sub box" @click="sub(i)">-</div>
          </div>
          <div class="remove_icon" @click="remove(i)">
            <font-awesome-icon :icon="['fas', 'trash']" />
          </div>
        </div>
        <h3 class="m_tprice">
          <span>Total Price :</span>{{ product.price * product.count }}$
        </h3>
        <div class="remove_icon_2" @click="remove(i)">
          <font-awesome-icon :icon="['fas', 'trash']" />
        </div>
      </div>
      <!-- Item Sum -->
      <h1 class="total">Total Price : {{ totalP }}$</h1>

      <!-- CheckOut Form -->
      <form action="" class="main_form">
        <h5>Delivery Addresses</h5>
        <div class="t_checkbox">
          <div class="radio_list">
            <div class="radiobox" v-for="(address, i) in dAdress" :key="i">
              <input
                type="radio"
                v-model="selected"
                :value="address.text"
                :id="address.id"
                name="address"
              />
              <label :for="address.id">{{ address.text }}</label>
            </div>
          </div>

          <div class="checkbox">
            <input type="checkbox" id="toggle" v-model="checked" />
            <label for="toggle"
              >Billing Address is same as Delivery Address</label
            >
          </div>
        </div>

      
       <!-- Billing Address -->
        <!-- <input
          type="text"
          v-if="!checked"
          placeholder="Billing Address"
          required
          v-model="billingAddress"
        /> -->

        <h5 v-if="!checked">Billing Addresses</h5>
        <div class="t_checkbox" v-if="!checked">
          <div class="radio_list">
            <div class="radiobox" v-for="(address, i) in bAdress" :key="i">
              <input
                type="radio"
                v-model="bSelected"
                :value="address.text"
                :id="address.id"
                name="Baddress"
              />
              <label :for="address.id">{{ address.text }}</label>
            </div>
          </div>
        </div>
      
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
          total: 0
        },
        {
          id: 2,
          title: "Google Pixel",
          variations: ["Black", "2GB Size"],
          img: require(`~/assets/images/2.jpg`),
          price: 10,
          count: 1,
          total: 0
        },
        {
          id: 3,
          title: "Google Pixel",
          variations: ["Black", "2GB Size"],
          img: require(`~/assets/images/3.jpg`),
          price: 10,
          count: 1,
          total: 0
        }
      ],
      checked: true,
      // Note : In order to get delivery address value use selected
      selected: "",
      bSelected:'',
      billingAddress:'',
      dAdress: [
        {
          id: 11,
          text: "G-11/2, Street 62, House 569, Islamabad"
        },
        {
          id: 22,
          text: "G-11/3, Street 62, House 569, Islamabad"
        },
        {
          id: 33,
          text: "G-11/4, Street 62, House 569, Islamabad"
        }
      ],
      bAdress: [
        {
          id: 13,
          text: "G-11/6, Street 62, House 569, Islamabad"
        },
        {
          id: 24,
          text: "G-11/7, Street 62, House 569, Islamabad"
        },
        {
          id: 36,
          text: "G-11/8, Street 62, House 569, Islamabad"
        }
      ]
    };
  },
  methods: {
    add(i) {
      this.Products[i].count += 1;
    },
    sub(i) {
      if (this.Products[i].count == 1) {
        return;
      }
      this.Products[i].count -= 1;
    },
    remove(i) {
      this.Products.splice(i, 1);
    }
  },
  computed: {
    totalP() {
      let amount = 0;
      this.Products.forEach(product => {
        amount += product.price * product.count;
      });
      return amount;
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
  font-family: "Nunito", sans-serif;

  background-color: #eee;

  .cart_inner {
    max-width: 1100px;
    margin: auto;
    width: 100%;
    padding: 10px;
    padding: 20px 5px;
    .title {
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
        font-size: 25px !important;
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
          @media (max-width: 580px) {
            flex: 0 0 100%;
            max-width: 100%;
            width: 100%;
            margin: 10px 0;
          }
          h1,
          p {
            text-align: left;
            @media (max-width: 580px) {
              text-align: center;
            }
          }
          h1 {
            font-size: 20px;
            font-weight: 500;
          }
          p {
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
          span {
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
          @media (max-width: 580px) {
            justify-content: center;
            flex: 0 0 100%;
            max-width: 100%;
          }
          .box {
            width: 30px;
            height: 30px;
            border: 2px solid #000;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 5px;
            cursor: pointer;
            transition: 0.3s linear;
            &:hover {
              background-color: #000;
              color: #fff;
              // border-color: #fff;
            }
          }
          .content {
            width: 30px;
            height: 30px;
            border: 2px solid #000;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 5px;
            transition: 0.3s linear;
             user-select: none;
            &:hover {
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
          @media (max-width: 580px) {
            display: none;
          }
          @media (max-width: 767px) {
            transform: translateX(0%);
          }
          svg {
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
      .remove_icon_2 {
        display: none;
        @media (max-width: 580px) {
          display: flex;
          flex: 0 0 100%;
          justify-content: center;
          max-width: 100%;
        }
        svg {
          color: red;
          cursor: pointer;
        }
      }
    }
    .total {
      text-align: right;
      @media(max-width:500px)
      {
        font-size: 20px;
      }
    }
    .main_form {
      max-width: 100%;
      width: 100%;
      // border: 2px solid red;
      padding: 20px;
      padding-left: 0;
      margin-top: 20px;
      h5 {
        border-bottom: 2px solid red;
        display: inline-block;
        padding: 5px;
        padding-left: 0;
        font-size: 25px;
        font-weight: bold;
         @media(max-width:500px)
      {
        font-size: 20px;
      }
      }
      .t_checkbox {
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        margin-bottom: 10px;
        .radio_list {
          flex: 0 0 50%;
          max-width: 50%;
          display: flex;
          flex-direction: column;
          @media(max-width:890px)
          {
             flex: 0 0 100%;
          max-width: 100%;
          }
          .radiobox {
            display: flex;
            align-items: center;
            background: #fff;
            margin: 5px 0;
           padding-left: 10px;
              label {
              margin-top: 10px;
              @media (max-width: 500px) {
                font-size: 16px;
              }
            }
            input {
              width: 17px;
              height: 17px;
              cursor: pointer;
            }
          }
        }
        .checkbox {
          display: flex;
          align-items: center;
          align-self: flex-start;
          transform: translateY(-20px);
          label {
            margin-top: 35px;
            @media (max-width: 470px) {
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
        &:focus {
          border: 2px solid #000;
          outline: none;
        }
      }
      #toggle {
        margin-top: 25px;
        width: 17px;
        height: 17px;
        cursor: pointer;
      }
      label {
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
        transition: 0.3s linear;
        background-color: red;
        font-weight: bold;
        cursor: pointer;
        text-decoration: none;
        &:focus {
          border: none;
          outline: none;
        }
        &:hover {
          background-color: #ffffff;
          color: #000;
          font-weight: bold;
          border: 1px solid red;
        }
      }
    }
  }
}
</style>
