import RowItem from '@/components/RowItem';
<template>
  <div className="dictionary">
    <h4 className="dictionary__amount">Список слов:</h4>
    <RowItem
      className="dictionary__item"
      v-for="dRow in dRows"
      :dRow="dRow"
      :key="dRow.id"
      @remove="$emit('remove', dRow)"
    />
  </div>
</template>

<script>
import RowItem from "@/components/RowItem";
export default {
  components: { RowItem },
  props: {
    dRows: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.dictionary__amount {
  font-size: 18px;
  margin-top: 5px;
  font-family: tahoma, sans-serif;
}
</style>
