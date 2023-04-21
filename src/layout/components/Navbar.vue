<template>
  <div>
    <nav
      class="navbar navbar-expand-lg navbar-dark bg-info fixed-top p-st"
    >
      <div class="container">
        <a
          class="navbar-brand"
          href="/"
          @click.prevent="$emit('scroll', 'home')"
        >
          <span><img style="width: 40px" :src="image" alt=""></span>
        </a>
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
                  <a href="#" style="text-decoration: none; color: #358827 !important;">ĐĂNG NHẬP</a>
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
                  <a v-b-modal.modal-center href="#" style="text-decoration: none; color: #358827 !important;">ĐĂNG KÝ</a>
                </div>
              </a>
            </li>
          </ul>

        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  components: {
  },
  props: {
    nightMode: {
      type: Boolean
    }
  },
  data() {
    return {
      image: require('/src/assets/logo/logo.jpg')
    }
  },
  methods: {
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

.logo-title-name {
  color: #358827;
  font-size: 35px;
  font-weight: 500;
  letter-spacing: 2px;
  transition: 0.5s all;
}

@media(max-width: 991px){
  .dropdown-content {
    /*display: none;*/
    min-width: 100%;
    position: relative;
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



{
  border: 0;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
:root {
  font-size: calc(16px + (24 - 16)*(100vw - 320px)/(1920 - 320));
}
body, button, input {
  font: 1em Hind, sans-serif;
  line-height: 1.5em;
}
body, input {
  color: #171717;
}
body, .search-bar {
  display: flex;
}
body {
  background: #f1f1f1;
  height: 100vh;
}
.search-bar input,
.search-btn,
.search-btn:before,
.search-btn:after {
  transition: all 0.25s ease-out;
}
.search-bar input,
.search-btn {
  width: 3em;
  height: 3em;
}
.search-bar input:invalid:not(:focus),
.search-btn {
  cursor: pointer;
}
.search-bar,
.search-bar input:focus,
.search-bar input:valid  {
  width: 100%;
}
.search-bar input:focus,
.search-bar input:not(:focus) + .search-btn:focus {
  outline: transparent;
}
.search-bar {
  margin: auto;
  padding: 1.5em;
  justify-content: center;
  max-width: 30em;
}
.search-bar input {
  background: transparent;
  border-radius: 1.5em;
  box-shadow: 0 0 0 0.4em #171717 inset;
  padding: 0.75em;
  transform: translate(0.5em,0.5em) scale(0.5);
  transform-origin: 100% 0;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
}
.search-bar input::-webkit-search-decoration {
  -webkit-appearance: none;
}
.search-bar input:focus,
.search-bar input:valid {
  background: #fff;
  border-radius: 0.375em 0 0 0.375em;
  box-shadow: 0 0 0 0.1em #d9d9d9 inset;
  transform: scale(1);
}
.search-btn {
  background: #171717;
  border-radius: 0 0.75em 0.75em 0 / 0 1.5em 1.5em 0;
  padding: 0.75em;
  position: relative;
  transform: translate(0.25em,0.25em) rotate(45deg) scale(0.25,0.125);
  transform-origin: 0 50%;
}
.search-btn:before,
.search-btn:after {
  content: "";
  display: block;
  opacity: 0;
  position: absolute;
}
.search-btn:before {
  border-radius: 50%;
  box-shadow: 0 0 0 0.2em #f1f1f1 inset;
  top: 0.75em;
  left: 0.75em;
  width: 1.2em;
  height: 1.2em;
}
.search-btn:after {
  background: #f1f1f1;
  border-radius: 0 0.25em 0.25em 0;
  top: 51%;
  left: 51%;
  width: 0.75em;
  height: 0.25em;
  transform: translate(0.2em,0) rotate(45deg);
  transform-origin: 0 50%;
}
.search-btn span {
  display: inline-block;
  overflow: hidden;
  width: 1px;
  height: 1px;
}

/* Active state */
.search-bar input:focus + .search-btn,
.search-bar input:valid + .search-btn {
  background: #2762f3;
  border-radius: 0 0.375em 0.375em 0;
  transform: scale(1);
}
.search-bar input:focus + .search-btn:before,
.search-bar input:focus + .search-btn:after,
.search-bar input:valid + .search-btn:before,
.search-bar input:valid + .search-btn:after {
  opacity: 1;
}
.search-bar input:focus + .search-btn:hover,
.search-bar input:valid + .search-btn:hover,
.search-bar input:valid:not(:focus) + .search-btn:focus {
  background: #0c48db;
}
.search-bar input:focus + .search-btn:active,
.search-bar input:valid + .search-btn:active {
  transform: translateY(1px);
}

@media screen and (prefers-color-scheme: dark) {
  body, input {
    color: #f1f1f1;
  }
  body {
    background: #171717;
  }
  .search-bar input {
    box-shadow: 0 0 0 0.4em #f1f1f1 inset;
  }
  .search-bar input:focus,
  .search-bar input:valid {
    background: #3d3d3d;
    box-shadow: 0 0 0 0.1em #3d3d3d inset;
  }
  .search-btn {
    background: #f1f1f1;
  }
}

</style>
