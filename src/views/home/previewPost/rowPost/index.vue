<template>
  <div class="container">
    <div class="row">
      <div
        v-for="(item,index) in data"
        :key="index"
        class="col-4 col-lg-3"
      >
        <div
          class="d-flex flex-column product-wrapper me-3"
        >
          <div class="img-wrapper mb-2 ">
            <img :src="item.img" class="prod-img">
          </div>
          <div class="text-center name-book">
            <span>{{ item.name }}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RowPost',
  props: {
    data: Array
  }
}
</script>

<style scoped>
.product-wrapper {
  box-sizing: border-box;
  box-shadow: 0 0 #0003;
  transition: box-shadow .2s cubic-bezier(.12, .98, .33, .99);
}

div.product-wrapper:hover {
  box-shadow: 0 2px 4px #0003;
}
@media (min-width: 400px) {
  .product-wrapper {
    width: 284px;
    height: 284px
  }
}

.img-wrapper{
  width: 284px;
  height: 284px
}
@media (max-width: 400px) {
  .product-wrapper .img-wrapper {
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
