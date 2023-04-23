<template>
  <div>
    <div class="container is-mobile py-3 padding-lg">
      <div class="row pt-1 ">
        <div class="col-12 search-bar ">
          <h3
            style="
          width: 268px;
          height: 89px;
          left: 182px;
          top: 2046px;
          font-family: 'Cooper Black', sans-serif;
          font-style: normal;
          font-weight: 400;
          font-size: 40px;
          line-height: 52px;
           color: #358827;
          "
          >CALLME</h3>
          <p style=" margin-top: -40px">Dịch vụ cung cấp nội dung hấp dẫn bổ ích</p>
        </div>
        <div class="col-3 align-items-center search-bar2">
          <h3
            style="
          width: 268px;
          height: 89px;
          left: 182px;
          top: 2046px;
          font-family: 'Cooper Black', sans-serif;
          font-style: normal;
          font-weight: 400;
          font-size: 40px;
          line-height: 52px;
           color: #358827;
          "
          >CALLME</h3>
          <p style="align-items: center; margin-top: -20px">DỊCH VỤ CUNG CẤP NỘI <br> DUNG HẤP DẪN BỔ ÍCH</p>
        </div>
        <div
          class="col-xl-6 col-bg-6 col-md-6 col-sm-12 pbelow align-items-left"
          style="color: black;"
        >
          <h4>THÔNG TIN</h4>
          <p style="font-size: 14px">Chủ sở hữu website: CÔNG TY CỔ PHẦN TRUYỀN THÔNG VMG <br>
            Tầng 6 Peakview Tower, 36 Hoàng Cầu, Quận Đống Đa, Hà Nội, Việt Nam <br>
            Điện thoại: 024-35378820 - Hotline: 19001255 <br>
            E-mail: info@vmgmedia.vn <br>
            Số Giấy chứng nhận kinh doanh: 0101883619 Ngày cấp: 10/02/2006 <br>
            Copyright © VMG Media <a href="https://www.facebook.com/ngocanh.thitep">Group</a></p>
        </div>
        <div class="col-12 align-items-center search-bar">
          <h4>QUY ĐỊNH</h4>
          <a href="#">Giới thiệu</a><br>
          <a href="#">Hướng dẫn</a><br>
          <a href="#">Điều khoản sử dụng</a>
        </div>
        <div class="col-3 align-items-center search-bar2">
          <h4>QUY ĐỊNH</h4>
          <a href="#">Giới thiệu</a><br>
          <a href="#">Hướng dẫn</a><br>
          <a href="#">Điều khoản sử dụng</a>
        </div>
      </div>

    </div></div></template>

<script>

export default {
  name: 'Footer',
  data() {
    return {

    }
  },
  methods: {

  }
}
</script>

<style scoped>
font {
  font-size: 14px;
  font-weight: 300;
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
/*@media screen and (max-width: 580px) {*/
/*  .pbelow {*/
/*    padding-bottom: 20px;*/
/*    text-align: left;*/
/*  }*/
/*}*/
</style>
