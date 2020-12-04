<template>
 
    <!--Navbar-->
    <mdb-navbar color="darken-3" class="m-0">
      <!-- mdbNavbar brand -->
      <mdb-navbar-brand class="text-black text-uppercase">
       YOURLOGO
      </mdb-navbar-brand>
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
                <div class="col-md-6 col-xl-3 sub-menu mb-0" v-for="(feature,i) in features" :key="i">
                  <h6
                    class="sub-title text-uppercase font-weight-bold black-text"
                  >
                   {{feature.title}}
                  </h6>
                 <ul class="list-unstyled m_list">               
                    <li v-for="(list,j) in feature.list" :key="j">
                      <img :src="list.img" alt="" />
                       <div class="p_detail">
                         <h6>{{list.name}}</h6>
                         <p>{{list.detail}}</p>
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
                <div class="col-md-6 col-xl-4 sub-menu mb-0" v-for="(feature,i) in technology" :key="i">
                  <h6
                    class="sub-title text-uppercase font-weight-bold black-text"
                  >
                   {{feature.title}}
                  </h6>
                 <ul class="list-unstyled m_list">               
                    <li v-for="(list,j) in feature.list" :key="j">
                      <img :src="list.img" alt="" />
                       <div class="p_detail">
                         <h6>{{list.name}}</h6>
                         <p>{{list.detail}}</p>
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
                <div class="col-md-6 col-xl-6 sub-menu mb-0" v-for="(feature,i) in life" :key="i">
                  <h6
                    class="sub-title text-uppercase font-weight-bold black-text"
                  >
                   {{feature.title}}
                  </h6>
                 <ul class="list-unstyled m_list">               
                    <li v-for="(list,j) in feature.list" :key="j">
                      <img :src="list.img" alt="" />
                       <div class="p_detail">
                         <h6>{{list.name}}</h6>
                         <p>{{list.detail}}</p>
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
  data(){
    return{
      features:[
        {
          title:'Design',
          list:[
            {
              img: require(`~/assets/images/1.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/2.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/3.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
          ]
        },
        {
          title:'Responsive',
          list:[
            {
              img:require(`~/assets/images/5.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/2.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/3.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
          ]
        },
        {
          title:'Standard',
          list:[
            {
              img:require(`~/assets/images/1.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/2.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/3.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
          ]
        },
        {
          title:'Pricing',
          list:[
            {
              img:require(`~/assets/images/1.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/2.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/3.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
          ]
        },
      ],
      technology:[
        {
          title:'Design',
          list:[
            {
              img: require(`~/assets/images/1.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/2.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/3.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
          ]
        },
        {
          title:'Responsive',
          list:[
            {
              img:require(`~/assets/images/5.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/2.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/3.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
          ]
        },
        {
          title:'Standard',
          list:[
            {
              img:require(`~/assets/images/1.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/2.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/3.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
          ]
        },
      ],
       life:[
        {
          title:'Design',
          list:[
            {
              img: require(`~/assets/images/1.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/2.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/3.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
          ]
        },
        {
          title:'Responsive',
          list:[
            {
              img:require(`~/assets/images/5.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/2.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
            {
              img:require(`~/assets/images/3.jpg`),
              name:'Product Name',
              detail:'Lorem ipsum dolor sit amet.'
            },
          ]
        }
      ]
    }
  }
};
</script>

<style lang="scss" scoped>
.feature_dd {
  width: 90vw;
  left: 50%;
  transform: translateX(-10%);
  @media(max-width:990px)
  {
    transform: translateX(0%);
  }
}
.tech_dd {
  width: 90vw;
  left: 50%;
  transform: translateX(-20%);
  @media(max-width:990px)
  {
    transform: translateX(0%);
  }
}
.life_dd {
  width: 90vw;
  left: 50%;
  transform: translateX(-30%);
  @media(max-width:990px)
  {
    transform: translateX(0%);
  }
 
}
 .m_list {
    li{
      margin: 5px 0;
      display: flex;
      cursor: pointer;
      transition: .3s linear;
      &:hover{

      background-color: #eee;


      }
      .p_detail{
        h6,p{
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
</style>
