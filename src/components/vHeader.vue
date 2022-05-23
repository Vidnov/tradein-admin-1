<template>
  <header>
    <nav>
      <el-menu
        :default-active="activeIndex"
        class="el-menu-demo"
        mode="horizontal"
        @select="handleSelect"
      >
        <el-menu-item index="1"> Главная </el-menu-item>
        <el-menu-item index="2">About</el-menu-item>
      </el-menu>
    </nav>
  </header>
</template>
<script>
export default {
  name: "vHeader",
  data() {
    return {};
  },
  computed: {
    activeIndex() {
      switch (this.$route.name) {
        case "home":
          return "1";
        case "about":
          return "2";
        default:
          return "0";
      }
    },
  },
  methods: {
    handleSelect(v) {
      switch (v) {
        case "1":
          this.$router.push("/");
          break;
        case "2":
          this.$router.push("/about");
          break;
        default:
          return;
      }
    },
  },
};
</script>
