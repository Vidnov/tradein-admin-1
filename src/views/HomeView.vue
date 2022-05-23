<template>
  <section>
    <el-header class="test">
      <v-table />
      <v-table />
      <v-table />
      <v-table />
      <v-table />
    </el-header>
  </section>
</template>

<script>
// @ is an alias to /src
import vTable from "../components/vTable.vue";

export default {
  name: "HomeView",
  mounted(){

  },
  components: {
    vTable,
  },
};
</script>
<style scoped>
section{
  margin: 0 auto;
  max-width: 1200px;
}
.test{
  display: grid;
  grid-gap: 20px;
  grid-template-columns: 1fr 1fr;
}
</style>