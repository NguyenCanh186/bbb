<template>
  <div class="d-flex flex-row">
    <div v-for="(item,index) in data" :key="index" class="text-center">
      <div class="margin-center service-item service-item__mobile">
        <span class="text-uppercase" style="color: #358827">{{ item.name }}</span>
        <span> gửi </span>
        <span style="color: #358827">{{ item.number }} </span>
        <span>{{ item.price }}</span>
        <span>.000đ/ngày</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ServiceItem',
  props: {
    data: Array
  }
}
</script>

<style scoped>
@media (max-width: 400px) {
  .service-item__mobile.service-item{
    width: 160px;
    height: 100px;
    margin-right: 15px;
    padding: 5px 8px 5px 8px;
    border: 1px solid #358827;
    border-radius: 10px;
    box-sizing: border-box;
    word-break: break-word;
    font-weight: 300;
    line-height: 18px;
    font-size: 18px;
  }

}
.service-item{
  box-sizing: border-box;
  word-break: break-word;
  font-weight: 400;
  line-height: 38px;
  font-size: 24px;
  width: 322px;
  height: 182px;
  margin-right: 100px;
  padding: 24px 35px 24px 33px;
  border: 1px solid #358827;
  border-radius: 25px;
}
</style>
