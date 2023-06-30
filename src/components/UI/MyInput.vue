<template>
  <input
    :value="modelValue"
    @input="updateInput"
    type="text"
    className="dictionary__addWord-input"
  />
</template>

<script>
export default {
  name: "MyInput",
  props: {
    modelValue: [String, Number],
  },
  methods: {
    updateInput(event) {
      this.$emit("update:modelValue", event.target.value);
    },
  },
};
</script>

<style scoped>
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
    width: 80%;
    margin: 10px 10px 10px 0;
  }
}

.dictionary__addWord-input {
  border: none;
  border: 3px solid orange;
  padding: 5px 5px;
  border-radius: 10px;
  margin: 10px 10px 0 0;
  font-size: 16px;
  outline: none;
}

.dictionary__addWord-input[type="text"] {
  padding: 12px 13px;
}
</style>
