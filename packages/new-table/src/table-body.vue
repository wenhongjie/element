<template>
  <tbody class="el-table__body">
    <el-table-row :row-data="row" :key="i" v-for="(row, i) of rows" />
  </tbody>
</template>

<script>
import ElTableRow from './table-row.vue'
export default {
  name: 'ElTableBody',

  components: {
    ElTableRow
  },

  inject: ['table'],

  computed: {
    rows() {
      return this.table.computedData
    }
  }
}
</script>
