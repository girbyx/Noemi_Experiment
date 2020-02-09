<template>
  <Wizard header="Survey/Wizard" class="wizard" />
</template>

<script>
import Wizard from "@/components/Wizard/Wizard.vue";

export default {
  name: "Survey",
  components: {
    Wizard
  }
};
</script>

<style lang="scss">
.wizard {
  width: 75%;
  margin: auto;
  border: 1px black solid;
  float: center;
}
</style>
