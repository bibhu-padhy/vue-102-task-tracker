<template>
  <button :class="btnCls">{{ text }}</button>
</template>

<script>
export default { 
  name: "Button",
  props: ["text", "btnCls"],
  methods: {
    onClick() {
      console.log("button clicked");
    },
  },
};
</script>

<style></style>
