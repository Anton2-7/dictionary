import MyButton from '@/components/UI/MyButton';
<template>
  <div className="dictionary__item">
    <div className="dictionary__word">
      {{ dRow.Ablock }}
    </div>
    <div className="dictionary__word">
      {{ dRow.Cblock }}
    </div>
    <div className="post__btn">
      <MyButton @click="$emit('remove', dRow)" className="btn remove--btn"
        >❌</MyButton
      >
    </div>
  </div>
</template>

<script>
export default {
  props: {
    dRow: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped>
.dictionary__word {
  font-family: "Trebuchet MS", Helvetica, sans-serif;
  font-width: 800;
  font-size: 20px;
}
.dictionary__item {
  display: flex;
  justify-content: space-around;
  margin-top: 20px;
  align-items: center;
  padding: 15px 10px;
  border-radius: 10px;
  -webkit-box-shadow: -1px 4px 8px 0px rgba(34, 60, 80, 0.2);
  -moz-box-shadow: -1px 4px 8px 0px rgba(34, 60, 80, 0.2);
  box-shadow: -1px 4px 8px 0px rgba(34, 60, 80, 0.2);
}
</style>
