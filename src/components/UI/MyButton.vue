<template>
  <button><slot></slot></button>
</template>

<script>
export default {
  name: "MyButton",
};
</script>

<style scoped>
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
@media (min-width: 100px) and (max-width: 500px) {
  .btn {
    padding: 15px !important;
    cursor: pointer;
    width: 100%;
    border: 2px solid;
  }
  .addNewRow--btn {
    otline: none;
    border-radius: 20px;
    color: #755d9a;
    font-family: tahoma, sans-serif;
    font-size: 14px;
    background: none;
    border: 3px solid #755d9a;
  }
}
.btn {
  padding: 5px 5px;
  cursor: pointer;
}
.addNewRow--btn {
  otline: none;
  border-radius: 20px;
  color: #755d9a;
  font-family: tahoma, sans-serif;
  font-size: 14px;
  padding: 10px 20px 10px 20px;
  background: none;
  border: 2px solid #755d9a;
  -webkit-box-shadow: 3px 4px 8px 0px rgba(34, 60, 80, 0.2);
  -moz-box-shadow: 3px 4px 8px 0px rgba(34, 60, 80, 0.2);
  box-shadow: 3px 4px 8px 0px rgba(34, 60, 80, 0.2);
}
.addNewRow--btn:active {
  otline: none;
  border-radius: 20px;
  color: white;
  font-family: tahoma, sans-serif;
  font-size: 14px;
  padding: 10px 20px 10px 20px;
  background: #755d9a;
  border: 2px solid #755d9a;
  -webkit-box-shadow: 3px 4px 8px 0px rgba(34, 60, 80, 0.2);
  -moz-box-shadow: 3px 4px 8px 0px rgba(34, 60, 80, 0.2);
  box-shadow: 3px 4px 8px 0px rgba(34, 60, 80, 0.2);
}
.remove--btn {
  outline: none;
  border: none;
  border-radius: 20px;
  background: none;
  -webkit-box-shadow: -1px 4px 8px 0px rgba(34, 60, 80, 0.2);
  -moz-box-shadow: -1px 4px 8px 0px rgba(34, 60, 80, 0.2);
  box-shadow: -1px 4px 8px 0px rgba(34, 60, 80, 0.2);
}
</style>
