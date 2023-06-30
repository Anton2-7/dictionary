<template>
  <div className="dialog" v-if="show" @click.stop="hideDialog">
    <div @click.stop className="dialog__content">
      <slot></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "MyDialog",
  props: {
    show: {
      type: Boolean,
      default: false,
    },
  },
  methods: {
    hideDialog() {
      this.$emit("update:show", false);
    },
  },
};
</script>

<style scoped>
.dialog {
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  position: fixed;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
}
@media (max-width: 700px) {
  .dialog__content {
    margin: auto;
    background: white;
    border-radius: 12px;
    min-height: 50px;
    padding: 40px;
  }
}
@media (min-width: 100px) and (max-width: 500px) {
  .dialog__content {
    margin: auto;
    background: white;
    border-radius: 12px;
    min-height: 50px;
    min-width: 300px;
    padding: 40px 20px 20px 20px !important;
  }
}

.dialog__content {
  margin: auto;
  background: white;
  border-radius: 12px;
  min-height: 50px;
  min-width: 300px;
  padding: 40px;
}
</style>
