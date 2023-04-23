<template>
  <transition name="dialog">
    <div v-if="active" class="dialog-backdrop" @click="handleBackdropClick">
      <div class="dialog-container" @click.stop>
        <div class="col-12 justify-content-center" style="background-color: #358827; color: white;">
          <p style="text-align: center;margin-top: 1em">ĐĂNG KÝ</p>
        </div>
        <div style="padding: 15px">
          <p>Xin chào thuê bao xxxxxxxxxx, Quý khách chưa đăng ký dịch vụ Callme. Chọn gói dịch vụ muốn đăng ký</p>
          <div class="ml-md-4">
            <div style="display: flex; flex-wrap: wrap;">
              <div style="display: flex; align-items: center; margin-right: 15px;">
                <input id="g1" type="radio" name="fav_language" value="3k" class="d-inline-block">
                <p for="3k" class="d-inline-block " style="margin-left: 5px; margin-bottom: 0; display: flex; align-items: center;">Gói giải trí tổng hợp: 3.000đ/ngày, gia hạn hàng ngày</p>
              </div>
              <div style="display: flex; align-items: center;">
                <input id="g2" type="radio" name="fav_language" value="3ksk" class="d-inline-block">
                <p for="3ksk" class="d-inline-block " style="margin-left: 5px; margin-bottom: 0; display: flex; align-items: center;">Gói tư vấn chăm sóc sức khỏe: 3.000đ/ngày, gia hạn hàng ngày</p>
              </div>
            </div>
          </div>
          <br>
          <p style="font-style: italic;">Trường hợp tài khoản của quý khách tại thời điểm trừ cước không đủ cước theo giá gói, trừ cước bằng 50% giá cước gói</p>
          <button class="d-flex justify-content-center mx-auto" style="display: inline-block; width: 200px; background-color: #358827; color: white; height: 40px; border: none; border-radius: 20px; text-align: center; line-height: 40px;">ĐĂNG KÝ</button>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>
export default {
  name: 'RegisterAccount',
  props: {
    active: { type: Boolean, default: false }
  },
  methods: {
    handleBackdropClick() {
      this.$emit('update:active', false)
    }
  }
}
</script>

<style scoped>
.col-12 {
  border-radius: 15px 15px 0 0;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50px;
  width: 100%;
}
.dialog-backdrop {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.5);
}

.dialog-container {
  border-radius: 20px;
  max-width: 600px;
  box-shadow: 0 11px 15px -7px rgba(0, 0, 0, 0.2), 0 24px 38px 3px rgba(0, 0, 0, 0.14), 0 9px 46px 8px rgba(0, 0, 0, 0.12);
  margin-top: 10%;
  margin-left: auto;
  margin-right: auto;
  padding: 0;
  background-color: #fff;
}
input[type='radio'] {
  accent-color: #358827;
}
@media only screen and (max-width: 768px) {
  .dialog-container {
    max-width: 330px;
    margin-top: 40%;
  }
}
.dialog-enter-active .dialog-container,
.dialog-leave-active .dialog-container {
  transition: transform 0.4s;
}
.dialog-enter .dialog-container,
.dialog-leave-to .dialog-container {
  transform: scale(0.9);
}
</style>
