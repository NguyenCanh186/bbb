<template>
  <div class="position-relative">
    <div class="mt-3 px-2 stick-after" style="height: fit-content">
      <el-carousel style="padding: 0; margin: 0;border-radius: 20px;box-shadow: 0 0 #0003;height: fit-content " indicator-position="outside">
        <el-carousel-item v-for=" (item,index) in data" :key="index">
          <img class="img-banner" :src="item" alt="">
        </el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>
<script>
export default {
  name: 'Banner',
  data() {
    return {
      data: ['https://vietteltelecom.vn/images_content/flc/banner-flc.jpg', 'https://media.vietteltelecom.vn/upload/ckfinder/images/banner-1-07(1).png', 'https://viettel.vn/images_content/trendy/hinh1.png',
        'https://cdn.tgdd.vn/Files/2020/10/07/1296856/cach-dang-ky-4g-trendy-viettel-1-_1539x600-800-resize.jpg']
    }
  }
}
</script>

<style >
.img-banner{
  height: 100%;
  width: 100%;
}
@media (min-width: 400px) {
  .el-carousel__container {
    height: 500px!important;
  }
  .stick-after:after{
    display: none;
  }
}
@media (max-width: 400px) {
  .img-banner {
    object-fit: cover;
  }

}
</style>
