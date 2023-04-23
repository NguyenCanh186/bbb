<template>
  <div>
    <transition name="dialog">
      <div v-if="active" class="dialog-backdrop" @click="handleBackdropClick">
        <div class="dialog-container" @click.stop>
          <div class="col-12 justify-content-center" style="background-color: #358827; color: white;">
            <p style="text-align: center;margin-top: 1em">ĐĂNG NHẬP</p>
          </div>
          <div style="padding: 20px 50px 20px 50px">
            <div style="display: flex; flex-wrap: wrap;">
              <div style="align-items: center; width: 100%">
                <label for="g1">Nhập số điện thoại</label><br>
                <input type="text" class="inputLogin"><br>
                <label for="g1">Nhập mật khẩu</label><br>
                <input type="text" class="inputLogin">
              </div>
            </div>
            <br>
            <button class="d-flex justify-content-center mx-auto" style="display: inline-block; width: 200px; background-color: #358827; color: white; height: 40px; border: none; border-radius: 20px; text-align: center; line-height: 40px;">ĐĂNG NHẬP</button>
          </div>
        </div>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'Login',
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
  width: 100%;
  height: 100%;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: rgba(0, 0, 0, 0.5) !important;
}

.dialog-container {
  border-radius: 20px;
  max-width: 450px;
  box-shadow: 0 11px 15px -7px rgba(0, 0, 0, 0.2), 0 24px 38px 3px rgba(0, 0, 0, 0.14), 0 9px 46px 8px rgba(0, 0, 0, 0.12) !important;
  margin-top: 10%;
  margin-left: auto;
  margin-right: auto;
  padding: 0;
  background-color: #fff;
}
.inputLogin {
  width: 100%;
  padding: 10px;
  box-sizing: border-box;
  height: 35px
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
