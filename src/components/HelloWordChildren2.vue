<template>
  <div> Eu sou o filho 2: {{ getShipments() }}</div>
</template>

<script>
export default {
  name: "HelloWordChildren",
  inject: ["getShipments"],
};
</script>

<style></style>
