import App from '../../../../PhpstormProjects/untitled/src/App';
<template>
  <header className="header">
    <div className="container">Англо-русский словарь</div>
  </header>
  <div className="container">
    <row-form @create="createRec" />
    <row-list :dRows="dRows" />
  </div>
</template>

<script>
import RowForm from "./components/RowForm";
import RowList from "./components/RowList.vue";

export default {
  components: {
    RowForm,
    RowList,
  },
  data() {
    return {
      dRows: [
        {
          id: 1,
          Ablock: "Hello",
          Cblock: "Привет",
        },
        {
          id: 2,
          Ablock: "Snake",
          Cblock: "Змея",
        },
        {
          id: 3,
          Ablock: "Bread",
          Cblock: "Хлеб",
        },
      ],
    };
  },
  methods: {
    createRec(dRow) {
      this.dRows.push(dRow);
    },
  },
};
</script>

<style>
* {
  padding: 0;
  margin: 0;
}

.dictionary {
  padding-top: 10px;
  color: black;
}

.container {
  max-width: 900px;
  padding: 0 15px;
  margin: 0 auto;
}
.header {
  padding: 20px 0;
  -webkit-box-shadow: 0px 5px 8px 0px rgba(34, 60, 80, 0.2);
  -moz-box-shadow: 0px 5px 8px 0px rgba(34, 60, 80, 0.2);
  box-shadow: 0px 5px 8px 0px rgba(34, 60, 80, 0.2);
  background: #fc4a1a; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #f7b733,
    #fc4a1a
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #f7b733,
    #fc4a1a
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
  color: white;
  font-family: arial, sans-serif;
  font-size: 19px;
}
</style>
