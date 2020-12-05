<template>
  <div class="main_nav">
    <!-- Cart Nav -->
    <div class="top_nav">
      <div class="logo">
        <span>
          <svg
            width="35"
            height="16"
            viewBox="0 0 35 16"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M1.82812 10.7734H7.21875V12H0.320312V0.625H1.82812V10.7734ZM8.32031 7.69531C8.32031 6.86719 8.48177 6.1224 8.80469 5.46094C9.13281 4.79948 9.58594 4.28906 10.1641 3.92969C10.7474 3.57031 11.4115 3.39062 12.1562 3.39062C13.3073 3.39062 14.237 3.78906 14.9453 4.58594C15.6589 5.38281 16.0156 6.44271 16.0156 7.76562V7.86719C16.0156 8.6901 15.8568 9.42969 15.5391 10.0859C15.2266 10.737 14.776 11.2448 14.1875 11.6094C13.6042 11.974 12.9323 12.1562 12.1719 12.1562C11.026 12.1562 10.0964 11.7578 9.38281 10.9609C8.67448 10.1641 8.32031 9.10938 8.32031 7.79688V7.69531ZM9.77344 7.86719C9.77344 8.80469 9.98958 9.55729 10.4219 10.125C10.8594 10.6927 11.4427 10.9766 12.1719 10.9766C12.9062 10.9766 13.4896 10.6901 13.9219 10.1172C14.3542 9.53906 14.5703 8.73177 14.5703 7.69531C14.5703 6.76823 14.349 6.01823 13.9062 5.44531C13.4688 4.86719 12.8854 4.57812 12.1562 4.57812C11.4427 4.57812 10.8672 4.86198 10.4297 5.42969C9.99219 5.9974 9.77344 6.8099 9.77344 7.86719ZM17.4844 7.70312C17.4844 6.38542 17.7891 5.33854 18.3984 4.5625C19.0078 3.78125 19.8151 3.39062 20.8203 3.39062C21.8516 3.39062 22.6562 3.75521 23.2344 4.48438L23.3047 3.54688H24.625V11.7969C24.625 12.8906 24.2995 13.7526 23.6484 14.3828C23.0026 15.013 22.1328 15.3281 21.0391 15.3281C20.4297 15.3281 19.8333 15.1979 19.25 14.9375C18.6667 14.6771 18.2214 14.3203 17.9141 13.8672L18.6641 13C19.2839 13.7656 20.0417 14.1484 20.9375 14.1484C21.6406 14.1484 22.1875 13.9505 22.5781 13.5547C22.974 13.1589 23.1719 12.6016 23.1719 11.8828V11.1562C22.5938 11.8229 21.8047 12.1562 20.8047 12.1562C19.8151 12.1562 19.013 11.7578 18.3984 10.9609C17.7891 10.1641 17.4844 9.07812 17.4844 7.70312ZM18.9375 7.86719C18.9375 8.82031 19.1328 9.57031 19.5234 10.1172C19.9141 10.6589 20.4609 10.9297 21.1641 10.9297C22.0755 10.9297 22.7448 10.5156 23.1719 9.6875V5.82812C22.7292 5.02083 22.0651 4.61719 21.1797 4.61719C20.4766 4.61719 19.9271 4.89062 19.5312 5.4375C19.1354 5.98438 18.9375 6.79427 18.9375 7.86719ZM26.4297 7.69531C26.4297 6.86719 26.5911 6.1224 26.9141 5.46094C27.2422 4.79948 27.6953 4.28906 28.2734 3.92969C28.8568 3.57031 29.5208 3.39062 30.2656 3.39062C31.4167 3.39062 32.3464 3.78906 33.0547 4.58594C33.7682 5.38281 34.125 6.44271 34.125 7.76562V7.86719C34.125 8.6901 33.9661 9.42969 33.6484 10.0859C33.3359 10.737 32.8854 11.2448 32.2969 11.6094C31.7135 11.974 31.0417 12.1562 30.2812 12.1562C29.1354 12.1562 28.2057 11.7578 27.4922 10.9609C26.7839 10.1641 26.4297 9.10938 26.4297 7.79688V7.69531ZM27.8828 7.86719C27.8828 8.80469 28.099 9.55729 28.5312 10.125C28.9688 10.6927 29.5521 10.9766 30.2812 10.9766C31.0156 10.9766 31.599 10.6901 32.0312 10.1172C32.4635 9.53906 32.6797 8.73177 32.6797 7.69531C32.6797 6.76823 32.4583 6.01823 32.0156 5.44531C31.5781 4.86719 30.9948 4.57812 30.2656 4.57812C29.5521 4.57812 28.9766 4.86198 28.5391 5.42969C28.1016 5.9974 27.8828 6.8099 27.8828 7.86719Z"
              fill="black"
            />
          </svg>
        </span>
      </div>

      <form class="top_form">
        <mdb-input
          type="search"
          class="input text-white"
          placeholder="Search"
          aria-label="Search"
          label
          navInput
          style="border-color:#000 !important;"
        />
      </form>
      <div class="btns">
        <router-link to="/">Login</router-link>
        <router-link to="/cart" tag="span">
          <svg
            width="32"
            height="30"
            viewBox="0 0 32 30"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M31.08 3.37001C30.8916 3.13773 30.6091 3.00198 30.31 3.00001H9.49001L10.14 5.00001H29L26.33 17H11.33L6.76001 2.53001C6.65968 2.21836 6.41315 1.97557 6.10001 1.88001L2.00001 0.620007C1.65704 0.514614 1.28389 0.600201 1.02113 0.844529C0.758366 1.08886 0.645912 1.45481 0.726126 1.80453C0.806341 2.15425 1.06704 2.43461 1.41001 2.54001L5.00001 3.64001L9.59001 18.14L7.95001 19.48L7.82001 19.61C6.9832 20.5744 6.94962 21.9973 7.74001 23C8.2927 23.6721 9.13089 24.043 10 24H26.69C27.2423 24 27.69 23.5523 27.69 23C27.69 22.4477 27.2423 22 26.69 22H9.84001C9.60581 21.992 9.39281 21.8622 9.27831 21.6578C9.16381 21.4533 9.16445 21.2039 9.28001 21L11.69 19H27.13C27.6067 19.0117 28.0253 18.6852 28.13 18.22L31.3 4.22001C31.3616 3.91791 31.2805 3.60427 31.08 3.37001ZM25 30C26.2427 30 27.25 28.9926 27.25 27.75C27.25 26.5074 26.2427 25.5 25 25.5C23.7574 25.5 22.75 26.5074 22.75 27.75C22.75 28.9926 23.7574 30 25 30ZM13.58 27.75C13.58 28.9926 12.5727 30 11.33 30C10.0874 30 9.08001 28.9926 9.08001 27.75C9.08001 26.5074 10.0874 25.5 11.33 25.5C12.5727 25.5 13.58 26.5074 13.58 27.75Z"
              fill="red"
            />
          </svg>
          <div class="cart-value">
            2
          </div>
        </router-link>
      </div>
    </div>
    <!-- Cart Nav -->
    <!--Navbar-->
    <mdb-navbar color="darken-3" class="m-0 shadow-none bottom_nav" light>
      <form class="bottom_form">
          <mdb-input
          type="search"
          class="text-white"
          placeholder="Search"
          aria-label="Search"
          label
          navInput
          style="border-color:#000 !important;"
          
        />
        </form>
      <mdb-navbar-toggler>
        <mdb-navbar-nav left>
          <!-- Featured Item -->
          <mdb-dropdown tag="li" megaMenu class="nav-item">
            <mdb-dropdown-toggle
              slot="toggle"
              class="text-uppercase"
              tag="a"
              transparent
              navLink
              waves-fixed
              >Features</mdb-dropdown-toggle
            >
            <mdb-dropdown-menu
              class="mega-menu v-2 z-depth-1 darken-3 py-5 px-3 feature_dd"
            >
              <div class="row">
                <div
                  class="col-md-6 col-xl-3 sub-menu mb-0"
                  v-for="(feature, i) in features"
                  :key="i"
                >
                  <ul class="list-unstyled m_list">
                    <li v-for="(list, j) in feature.list" :key="j">
                      <img :src="list.img" alt="" />
                      <div class="p_detail">
                        <h6>{{ list.name }}</h6>
                        <p>{{ list.detail }}</p>
                      </div>
                    </li>
                  </ul>
                </div>
              </div>
            </mdb-dropdown-menu>
          </mdb-dropdown>
          <!-- Featured Item -->
          <!-- Techor -->
          <mdb-dropdown tag="li" megaMenu class="nav-item">
            <mdb-dropdown-toggle
              slot="toggle"
              class="text-uppercase"
              tag="a"
              transparent
              navLink
              waves-fixed
              >Technology</mdb-dropdown-toggle
            >
            <mdb-dropdown-menu
              class="mega-menu v-2 z-depth-1 darken-3 py-5 px-3 tech_dd"
            >
              <div class="row">
                <div
                  class="col-md-6 col-xl-4 sub-menu mb-0"
                  v-for="(feature, i) in technology"
                  :key="i"
                >
                  <ul class="list-unstyled m_list">
                    <li v-for="(list, j) in feature.list" :key="j">
                      <img :src="list.img" alt="" />
                      <div class="p_detail">
                        <h6>{{ list.name }}</h6>
                        <p>{{ list.detail }}</p>
                      </div>
                    </li>
                  </ul>
                </div>
              </div>
            </mdb-dropdown-menu>
          </mdb-dropdown>
          <!-- Techor -->

          <!-- LifStyled -->
          <mdb-dropdown tag="li" megaMenu class="nav-item">
            <mdb-dropdown-toggle
              slot="toggle"
              class="text-uppercase"
              tag="a"
              transparent
              navLink
              waves-fixed
              >Lifestyle</mdb-dropdown-toggle
            >
            <mdb-dropdown-menu
              class="mega-menu v-2 z-depth-1 darken-3 py-5 px-3 life_dd"
            >
              <div class="row">
                <div
                  class="col-md-6 col-xl-6 sub-menu mb-0"
                  v-for="(feature, i) in life"
                  :key="i"
                >
                  <ul class="list-unstyled m_list">
                    <li v-for="(list, j) in feature.list" :key="j">
                      <img :src="list.img" alt="" />
                      <div class="p_detail">
                        <h6>{{ list.name }}</h6>
                        <p>{{ list.detail }}</p>
                      </div>
                    </li>
                  </ul>
                </div>
              </div>
            </mdb-dropdown-menu>
          </mdb-dropdown>
          <!-- LifStyled -->
        </mdb-navbar-nav>
      </mdb-navbar-toggler>
    </mdb-navbar>
    <!--/.Navbar-->
  </div>
</template>

<script>
import {
  mdbContainer,
  mdbRow,
  mdbIcon,
  mdbNavbar,
  mdbNavbarBrand,
  mdbNavbarToggler,
  mdbNavbarNav,
  mdbNavItem,
  mdbInput,
  mdbDropdown,
  mdbDropdownToggle,
  mdbDropdownMenu,
  mdbDropdownItem
} from "mdbvue";
export default {
  name: "MegaMenuPage",
  components: {
    mdbContainer,
    mdbRow,
    mdbIcon,
    mdbNavbar,
    mdbNavbarBrand,
    mdbNavbarToggler,
    mdbNavbarNav,
    mdbNavItem,
    mdbInput,
    mdbDropdown,
    mdbDropdownToggle,
    mdbDropdownMenu,
    mdbDropdownItem
  },
  data() {
    return {
      features: [
        {
          title: "Design",
          list: [
            {
              img: require(`~/assets/images/1.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/2.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/3.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            }
          ]
        },
        {
          title: "Responsive",
          list: [
            {
              img: require(`~/assets/images/5.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/2.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/3.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            }
          ]
        },
        {
          title: "Standard",
          list: [
            {
              img: require(`~/assets/images/1.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/2.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/3.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            }
          ]
        },
        {
          title: "Pricing",
          list: [
            {
              img: require(`~/assets/images/1.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/2.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/3.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            }
          ]
        }
      ],
      technology: [
        {
          title: "Design",
          list: [
            {
              img: require(`~/assets/images/1.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/2.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/3.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            }
          ]
        },
        {
          title: "Responsive",
          list: [
            {
              img: require(`~/assets/images/5.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/2.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/3.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            }
          ]
        },
        {
          title: "Standard",
          list: [
            {
              img: require(`~/assets/images/1.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/2.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/3.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            }
          ]
        }
      ],
      life: [
        {
          title: "Design",
          list: [
            {
              img: require(`~/assets/images/1.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/2.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/3.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            }
          ]
        },
        {
          title: "Responsive",
          list: [
            {
              img: require(`~/assets/images/5.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/2.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            },
            {
              img: require(`~/assets/images/3.jpg`),
              name: "Product Name",
              detail: "Lorem ipsum dolor sit amet."
            }
          ]
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.feature_dd {
  width: 90vw;
  left: 50%;
  transform: translateX(0%);
  @media (max-width: 990px) {
    transform: translateX(0%);
  }
}
.tech_dd {
  width: 90vw;
  left: 50%;
  transform: translateX(-2%);
  @media (max-width: 990px) {
    transform: translateX(0%);
  }
}
.life_dd {
  width: 90vw;
  left: 50%;
  transform: translateX(-17%);
 
   @media (max-width: 990px) {
    transform: translateX(0%);
  }
  
 
}
.m_list {
  li {
    margin: 5px 0;
    display: flex;
    cursor: pointer;
    transition: 0.3s linear;
    &:hover {
      background-color: #eee;
    }
    .p_detail {
      h6,
      p {
        margin: 0;
      }
      display: flex;
      flex-direction: column;
      justify-content: center;
    }
  }
  img {
    width: 60px;
    height: 60px;
    margin-right: 10px;
  }
}
.bottom_form {
  display: none;
  @media (max-width: 990px) {
    display: block;
  }
}
.top_form {
  @media (max-width: 990px) {
    display: none;
  }
}
.top_nav {
  width: 100%;
  display: flex;
  justify-content: space-between;
  height: 60px;
  align-items: center;
  padding: 0 20px;
  border-bottom: 1px solid #000;
  a {
    margin-right: 33px;
    color: #000;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 19px;

    color: red;
  }
  .btns {
    svg {
      color: red;
    }
    span {
      position: relative;
      cursor: pointer;
      .cart-value {
        position: absolute;
        width: 19px;
        height: 19px;
        background-color: #000;
        color: #fff;
        left: 24px;
        top: -4px;
        font-style: normal;
        font-weight: 500;
        font-size: 12px;
        color: #ffffff;
        border-radius: 50%;
        display: flex;
        justify-content: center;
      }
    }
  }
}
.main_nav {
  border-bottom: 1px solid #000;
}
.bottom_nav{
  min-height: 59px;
}
</style>
