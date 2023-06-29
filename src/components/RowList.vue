<template>
  <div className="dictionary">
    <h4>Список слов:</h4>
    <row-item
      className="dictionary__item"
      v-for="dRow in dRows"
      :dRow="dRow"
      :key="dRow.id"
    />
  </div>
</template>

<script>
import RowItem from "@/components/RowItem";
export default {
  component: { RowItem },
  props: {
    dRows: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped></style>
