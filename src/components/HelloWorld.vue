<template>
  <div>
    Sou o pai e to provendo:
    {{ getShipments() }}
    
    <br>
    <br>
    <HelloWordChildren />
  </div>
</template>

<script>
import HelloWordChildren from "./HelloWordChildren.vue";

const getShipmentsService = () => ({
  common: {
    a: "b",
  },
  custom: {
    c: "d",
  },
});

export default {
  name: "HelloWord",
  components: { HelloWordChildren },
  provide() {
    return {
      getShipments: this.getShipments,
    };
  },
  methods: {
    getShipments() {
      return getShipmentsService();
    },
  },
};
</script>
