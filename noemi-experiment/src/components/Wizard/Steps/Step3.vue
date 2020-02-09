<template>
  <v-row>
    <v-col sm="12">
      <h1>Do you have some additional comments?</h1>
    </v-col>
    <v-col sm="12">
      <div>
        <textarea rows="15" cols="90"></textarea>
      </div>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Step3 extends Vue {
}
</script>

<style lang="scss">
textarea {
  border: 1px black solid;
  resize: none;
}
</style>
