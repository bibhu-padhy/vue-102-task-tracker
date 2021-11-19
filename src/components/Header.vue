<template>
  <header>
    <h3>
      {{ title }}
    </h3>
    <Button btnCls="btn btn-secondary btn-sm" text="Add Task" />
  </header>
</template>

<script>
import Button from "../components/Button.vue";
export default {
  name: "Header",
  components: { Button },
  props: ["title"],
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
