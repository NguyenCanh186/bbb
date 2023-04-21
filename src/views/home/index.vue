<template>
  <div>
    <SignUp />
    <Banner />
    <div class="is-mobile py-3 px-3">
      <div class="padding-lg">
        <div class="container padding-md">
          <div class="d-flex flex-row justify-content-between align-self-center">
            <h1 class="text-subject">Mới nhất</h1>
            <span class="text-md-green">Tất cả</span>
          </div>
        </div>
        <RowPost :data="data" />
      </div>
      <div class="mt-4 position-relative padding-lg">
        <div class="container padding-md">
          <div class="d-flex flex-row justify-content-between align-self-center stick-after">
            <h2 class="text-subject">Nghe nhiều nhất</h2>
            <span class="text-md-green ">Tất cả</span>
          </div>
        </div>
        <ColumnPost :data="data" />
      </div>
      <ServicePack class="mt-3" />
      <div class="padding-lg">
        <div class="container padding-md">
          <div class="d-flex flex-row justify-content-between align-self-center">
            <h1 class="text-subject">Kho truyện</h1>
            <span class="text-md-green">Tất cả</span>
          </div>
        </div>
        <RowPost :data="data" />
      </div>
      <div class="padding-lg">
        <div class="container padding-md">
          <div class="d-flex flex-row justify-content-between align-self-center">
            <h1 class="text-subject">Giáo dục giới tính</h1>
            <span class="text-md-green">Tất cả</span>
          </div>
        </div>
        <RowPost :data="data" />
      </div>
    </div>
  </div>
</template>

<script>
import Banner from '@/components/Banner/Banner.vue'
import ColumnPost from '@/views/home/previewPost/collumPost/index.vue'
import RowPost from '@/views/home/previewPost/rowPost/index.vue'
import ServicePack from '@/components/ServicePack/ServicePack.vue'
import SignUp from '@/components/PopUp/SignUp/index.vue'
export default {
  name: 'IndexVue',
  components: { SignUp, ServicePack, RowPost, ColumnPost, Banner },
  data() {
    return {
      data: [
        {
          name: ' Thao túng tâm lý',
          img: 'https://newshop.vn/public/uploads/products/50678/sach-thao-tung-tam-ly-nhan-dien-thuc-tinh-va-chua-lanh-nhung-ton-thuong-tiem-an.jpg',
          author: 'Shannon Thomas',
          view: 221.1
        },
        {
          name: ' Thao túng tâm lý',
          img: 'https://newshop.vn/public/uploads/products/50678/sach-thao-tung-tam-ly-nhan-dien-thuc-tinh-va-chua-lanh-nhung-ton-thuong-tiem-an.jpg',
          author: 'Shannon Thomas',
          view: 221.1
        },
        {
          name: ' Thao túng tâm lý',
          img: 'https://newshop.vn/public/uploads/products/50678/sach-thao-tung-tam-ly-nhan-dien-thuc-tinh-va-chua-lanh-nhung-ton-thuong-tiem-an.jpg',
          author: 'Shannon Thomas',
          view: 221.1
        },
        {
          name: ' Thao túng tâm lý',
          img: 'https://newshop.vn/public/uploads/products/50678/sach-thao-tung-tam-ly-nhan-dien-thuc-tinh-va-chua-lanh-nhung-ton-thuong-tiem-an.jpg',
          author: 'Shannon Thomas',
          view: 221.1
        }
      ]
    }
  },
  computed: {
  }
}
</script>

<style scoped>
.padding-lg{
  margin-bottom: 20px;
}
@media (min-width: 400px) {
  .text-subject{
    font-style: normal;
    font-weight: 700;
    font-size: 23px;
    line-height: 20px;
    color: #000000;
  }
  .text-md-green{
    font-size: 16px;
    line-height: 20px;
  }
}
@media (min-width: 400px) {
  .is-mobile {
    width: 1248px;
    padding-right: 24px;
    padding-left: 24px;
    margin-right: auto;
    margin-left: auto;
    max-width: 100%;
  }
  .padding-lg{
    margin-bottom: 100px;
  }
  .padding-md{
    margin-top: 20px;
    margin-bottom: 30px;
  }
}
</style>
