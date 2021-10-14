<template>
  <div class="data-table">
    <h1><slot name="header"></slot></h1>
    <table>
      <thead>
        <tr>
          <th v-for="head of headers" :key="head">{{ head.text }}</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="it of items" :key="it">
          <td>{{ it.name }}</td>
          <td>{{ it.calories }}</td>
          <td>{{ it.fat }}</td>
          <td>{{ it.carbs }}</td>
          <td>{{ it.protein }}</td>
          <td>{{ it.iron }}</td>
        </tr>
        <slot name="bodyappend"></slot>
      </tbody>
    </table>
    <footer><slot name="footer"></slot></footer>
  </div>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
    },
    headers: {
      type: Array,
    },
  },
};
</script>

<style scoped>
.data-table {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  margin: 40px;
  border-collapse: collapse;
  font-size: 0.9em;
  font-family: sans-serif;
  min-width: 400px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
}
.data-table td,
th {
  text-align: left;
}
.data-table footer {
  margin: 30px 0 30px 0;
  font-style: italic;
}
.data-table thead tr {
  background-color: #009879;
  color: #ffffff;
  text-align: left;
}
.data-table th,
.data-table td {
  padding: 12px 15px;
}
.data-table tbody tr {
  border-bottom: 1px solid #dddddd;
}
.data-table tbody tr:nth-of-type(even) {
  background-color: #f3f3f3;
}
</style>
