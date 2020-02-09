<template>
  <div>
    <Wizard header="Survey/Wizard" class="wizard" />
  </div>
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
  width: 60%;
  min-height: 400px;
  margin: auto;
  border: 1px black solid;
  float: center;
}
</style>
