<template>
  <div>
    <div class="text-center button align-self-center margin-center">Đăng ký gói nội dung</div>
    <div class="py-4 ">
      <VueSlickCarousel style="width: 100%;height: 80%;" v-bind="settings">
        <ServiceItem :data="data" />
      </VueSlickCarousel>
    </div>
  </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'
import ServiceItem from '@/components/ServicePack/item/ServiceItem.vue'
export default {
  name: 'ServicePack',
  components: { ServiceItem, VueSlickCarousel },
  data() {
    return {
      settings: {
        'focusOnSelect': true,
        'infinite': false,
        'slidesToShow': 2,
        'speed': 500
      },
      data: [
        {
          name: 'Gói giải trí tổng hợp DK',
          number: 1082,
          price: 3
        },
        {
          name: 'Gói giải trí tổng hợp DK1',
          number: 1082,
          price: 3
        },
        {
          name: 'Gói giải trí tổng hợp DK',
          number: 1082,
          price: 3
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>
