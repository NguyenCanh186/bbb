<template>
  <div>
    <nav
      class="navbar navbar-expand-lg navbar-dark bg-info fixed-top1 p-st"
    >
      <div class="container">
        <a
          class="navbar-brand"
          href="/"
          @click.prevent="$emit('scroll', 'home')"
        >
          <span><img style="width: 40px" :src="image" alt=""></span>
        </a>
        <div id="navbarSupportedContent2" class="search-bar">
          <ul class="navbar-nav ml-auto">
            <div class="dropdown">
              <div class="topnav">
                <input class="inputSearch" type="text">
                <button class="buttonSearch" type="submit"><i class="fa fa-search" aria-hidden="true" /></button>
              </div>
            </div>
          </ul>
        </div>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span
            style="color: gray; font-size: 23px;"
          ><i class="fas fa-bars" />
          </span>
        </button>
        <div id="navbarSupportedContent" class="collapse navbar-collapse">
          <ul class="navbar-nav ml-auto">
            <li class="nav-item mx-2">
              <a
                class="nav-link"
                href="#"
                :class="{ 'text-light': nightMode }"
                @click.prevent="$emit('scroll', 'portfolio')"
              >
                <div class="dropdown">
                  <a href="#" style="text-decoration: none; color: #358827 !important;">GIẢI TRÍ TỔNG HỢP <i class="fa fa-caret-down" /></a>
                  <div class="dropdown-content">
                    <div class="product">
                      <a href="#">Kho truyện</a>
                    </div>
                    <div class="product">
                      <a href="#">Âm nhạc</a>
                    </div>
                    <div class="product">
                      <a href="#">Kinh tế</a>
                    </div>
                    <div class="product">
                      <a href="#">Tin tức</a>
                    </div>
                  </div>
                </div>
              </a>
            </li>
            <li class="nav-item mx-2">
              <a
                class="nav-link"
                href="#"
                :class="{ 'text-light': nightMode }"
                @click.prevent="$emit('scroll', 'portfolio')"
              >
                <div class="dropdown">
                  <a href="#" style="text-decoration: none; color: #358827 !important;">GÓI TƯ VẪN CHĂM SÓC SỨC KHỎE <i class="fa fa-caret-down" /></a>
                  <div class="dropdown-content">
                    <div class="product">
                      <a href="#">Giáo dục giới tính</a>
                    </div>
                    <div class="product">
                      <a href="#">Chàng - Nàng</a>
                    </div>
                    <div class="product">
                      <a href="#">Sức khỏe</a>
                    </div>
                    <div class="product">
                      <a href="#">Tâm sự thầm kín</a>
                    </div>
                    <div class="product">
                      <a href="#">Truyện tình lãng mạn</a>
                    </div>
                  </div>
                </div>
              </a>
            </li>
            <li class="nav-item mx-2">
              <a
                class="nav-link"
                href="#"
                :class="{ 'text-light': nightMode }"
                @click.prevent="$emit('scroll', 'portfolio')"
              >
                <div class="dropdown">
                  <a href="#" style="text-decoration: none; color: #358827 !important;">XEM NHIỀU NHẤT</a>
                </div>
              </a>
            </li>
          </ul>
        </div>
        <div id="navbarSupportedContent2" class="search-bar2">
          <ul class="navbar-nav ml-auto">
            <div class="dropdown">
              <div class="topnav">
                <input class="inputSearch" type="text">
                <button class="buttonSearch" type="submit"><i class="fa fa-search" aria-hidden="true" /></button>
              </div>
            </div>
          </ul>
        </div>
        <div id="navbarSupportedContent" style="margin-right: -80px" class="collapse navbar-collapse">
          <ul class="navbar-nav ml-auto">
            <li class="nav-item mx-2">
              <a
                class="nav-link"
                href="#"
                :class="{ 'text-light': nightMode }"
                @click.prevent="$emit('scroll', 'portfolio')"
              >
                <div class="dropdown">
                  <a type="button" style="text-decoration: none; color: #358827 !important;" @click="showLogin = !showLogin; ">ĐĂNG NHẬP</a>
                </div>
              </a>
            </li>
            <li class="nav-item mx-2">
              <a
                class="nav-link"
                href="#"
                :class="{ 'text-light': nightMode }"
                @click.prevent="$emit('scroll', 'portfolio')"
              >
                <div class="dropdown">
                  <a type="button" style="text-decoration: none; color: #358827 !important;" @click="show = !show">ĐĂNG KÝ</a>
                  <!--                  <a v-b-modal.modal-center href="#" style="text-decoration: none; color: #358827 !important;">ĐĂNG KÝ</a>-->
                </div>
              </a>
            </li>
          </ul>

        </div>
      </div>
    </nav>
    <div>
      <register-account :active.sync="show">
        <h1>Test</h1>
        <button type="button" @click="show = !show">Close</button>
      </register-account>
      <Login :active.sync="showLogin">
        <h1>Test</h1>
        <button type="button" @click="showLogin = !showLogin">Close</button>
      </Login>
    </div>
  </div>
</template>

<script>
import { max } from '@popperjs/core/lib/utils/math'
import { style } from 'svgo/lib/svgo/jsAPI'
import registerAccount from '@/components/PopUp/SignUp/registerAccount.vue'
import Login from '@/components/PopUp/SignUp/Login.vue'

export default {
  name: 'Navbar',
  components: {
    registerAccount,
    Login
  },
  props: {
    nightMode: {
      type: Boolean
    }
  },
  data() {
    return {
      image: require('/src/assets/logo/logo.jpg'),
      show: false,
      showLogin: false
    }
  },
  methods: {
    style() {
      return style
    },
    max
  }
}
</script>

<style scoped>
.nav-link {
  color: #358827;
  font-weight: 500;
}
.nav-link:hover{
}

.bg-info {
  background-color: #ffffff !important;
}

button {
  border: none;
  outline: none;
}

button:hover {
  border: none;
  outline: none;
}

nav {
  border-bottom: 1px solid rgba(160, 159, 159, 0.336);
  position: fixed !important;
}

.navbar-blur {
  backdrop-filter: blur(12px);
}

.navbar {
  background-color: #333;
  color: #358827;
  display: flex;
  justify-content: space-between;
  padding: 10px;
}

.dropdown {
  position: relative;
}

.dropdown-content {
  background-color: #ffffff;
  border-radius: 0 0 5px 5px;
  display: none;
  min-width: 160px;
  padding: 10px 0;
  position: absolute;
  right: 0;
  text-align: left;
  top: 100%;
  z-index: 1;
}

.dropdown-content a {
  color: #358827 !important;
  display: block;
  padding: 10px;
  text-decoration: none;
}

.dropdown-content a:hover {
  background-color: #fff;
  color: #358827
}

.dropdown:hover .dropdown-content {
  display: block;
}

.product {
  display: flex;
  align-items: center;
  position: relative;
  z-index: 2;
}

.product:hover .dropdown-options {
  display: flex;
}

.dropdown-options {
  color: #fff;
  display: none;
  flex-direction: column;
  position: absolute;
  background-color: #17a2b8;
  border-radius: 0 5px 5px 5px;
  min-width: 160px;
  padding: 10px 0;
  right: 0;
  text-align: left;
  top: 0;
  left: 100%;
  z-index: 1;
}

.dropdown-options a:hover {
  background-color: #fff;
  color: #17a2b8;
}
.option:hover {
  color: #17a2b8 !important
}

.inputSearch {
  /*border: 1px;*/
  border-color: #358827 !important;
  border-radius: 25px 0 0 25px !important;
}

.buttonSearch {
  color: white;
  display: inline;
  height: 30px;
  background-color: #358827 !important;
  border-radius: 0 25px 25px 0 !important;
}

.inputSearch, .buttonSearch {
  margin-top: -10px;
}
.logo-title-name {
  color: #358827;
  font-size: 35px;
  font-weight: 500;
  letter-spacing: 2px;
  transition: 0.5s all;
}

@media (max-width: 1399px) {
  .inputSearch {
    width: 120px;
  }
}

@media (max-width: 1199px) {
  .topnav {
    display: flex;
    align-items: center;
  }

  .inputSearch {
    width: 30px;
  }

  .buttonSearch {
    display: block;
  }
}

@media (max-width: 991px) {
  .search-bar {
    display: block; /* hiển thị phần tử */
  }
}

@media (min-width: 992px) {
  .search-bar {
    display: none; /* ẩn phần tử */
  }
}

@media (max-width: 991px) {
  .search-bar2 {
    display: none; /* hiển thị phần tử */
  }
}

@media (min-width: 992px) {
  .search-bar2 {
    display: block; /* ẩn phần tử */
  }
}

@media(max-width: 991px){
  .dropdown-content {
    /*display: none;*/
    min-width: 100%;
    position: relative;
  }

  .inputSearch {
    width: 140px;
    height: 30px;
  }

  .dropdown-options {
    display: none;
    min-width: 100%;
    position: unset;
  }
  .product{
    flex-direction: column;
    align-items: unset;
  }
}
.fixed-top1 {
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
   /*z-index: 1030;*/
}

</style>
