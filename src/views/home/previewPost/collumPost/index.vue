<template>
  <div class="container">
    <div v-for="(item,index) in data" :key="index">
      <div class="d-flex flex-row product-wrapper-col">
        <div class="img-wrapper-col mb-4 col-3">
          <img :src="item.img" class="prod-img">
        </div>
        <div class="mt-2 ms-4 col-9 text-lg-center pt-lg-4">
          <span class="fw-bold">{{ item.name }}</span>
          <div>{{ item.author }}</div>
          <div>{{ item.view }}k lượt nghe</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ColumnPost',
  props: {
    data: Array
  }

}
</script>

<style scoped>
.product-wrapper-col {
  box-sizing: border-box;
  box-shadow: 0 0 #0003;
  transition: box-shadow .2s cubic-bezier(.12, .98, .33, .99);
}

div.product-wrapper-col:hover {
  box-shadow: 0 2px 4px #0003;
}
.product-wrapper-col .img-wrapper-col{
  width: 284px;
  height: 284px
}
@media (max-width: 400px) {
  .product-wrapper-col .img-wrapper-col {
    width: 100px;
    height: 150px
  }
}

.prod-img{
  height: 100%;
  width: 100%;
}
@media (max-width: 400px) {
  .prod-img {
    object-fit: cover;
  }
}

</style>
