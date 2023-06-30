<template>
  <div className="dictionary__AddWord">
    <h4 className="dictionary__section">Добавить новый перевод</h4>

    <form @submit.prevent>
      <MyInput v-model="dRow.Ablock" type="text" placeholder="Введите слово" />
      <MyInput v-model="dRow.Cblock" type="text" placeholder="Введите слово" />
      <MyButton className="btn btn addWord--btn " @click="createRec">
        Добавить
      </MyButton>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dRow: {
        Ablock: "",
        Cblock: "",
      },
    };
  },
  methods: {
    createRec() {
      this.dRow.id = Date.now();
      this.$emit("create", this.dRow);
      this.dRow = {
        Ablock: "",
        Cblock: "",
      };
    },
  },
};
</script>

<style scoped>
.dictionary__AddWord {
  font-family: "Trebuchet MS", Helvetica, sans-serif;
  font-width: 800;
  font-size: 20px;
  flex-direction: row;
  margin: 0 auto;
}
@media (min-width: 100px) and (max-width: 500px) {
  .dictionary__section {
    margin-bottom: 20px;
  }
}
</style>
