<template>
  <div className="dictionary__AddWord">
    <h2 className="dictionary__section">Добавить новый перевод</h2>

    <form @submit.prevent>
      <input
        v-model="dRow.Ablock"
        className="dictionary__addWord-input"
        type="text"
        placeholder="Введите слово"
      />
      <input
        id="second-form"
        v-model="dRow.Cblock"
        className="dictionary__addWord-input"
        type="text"
        placeholder="Введите слово"
      />
      <button className="btn btn addWord--btn " @click="createRec">
        Добавить
      </button>
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
@media (max-width: 767.99px) {
  .dictionary__addWord-input {
    border: none;

    padding: 10px 5px;
    border-radius: 10px;
    width: auto;
    min-width: 91%;
    margin: 10px 10px 0 0;
    display: flex;
    flex-direction: row;
  }
  .addWord--btn {
    padding: 10px;
    font-family: Tahoma, sans-serif;
    font-width: bold;
    font-size: 13px;
    outline: none;
    border: 2px solid gray;
    background: none;
    border-radius: 20px;
    width: 100%;
    margin: 10px 10px 10px 0;
  }
}
.addWord--btn {
  padding: 20px;
  font-family: Tahoma, sans-serif;
  font-width: bold;
  font-size: 13px;
  outline: none;
  border: 2px solid gray;
  background: none;
  border-radius: 20px;
  margin: 10px 10px 10px 0;
}
.dictionary__addWord-input {
  border: none;
  border: 3px solid orange;
  padding: 10px 5px;
  border-radius: 10px;
  margin: 10px 10px 0 0;
  font-size: 16px;
  outline: none;
}

.dictionary__addWord-input[type="text"] {
  padding: 12px 13px;
}
.dictionary__section {
  margin-top: 20px;
  margin-bottom: 10px;
}
.btn {
  padding: 5px 10px;
  cursor: pointer;
}
</style>
