<template>
  <v-row>
    <v-col sm="12">
      <h1>What is your space purpose?</h1>
    </v-col>
    <v-col sm="4">
      <div>
        <input name="space" type="radio" /><span> Living Room</span>
      </div>
    </v-col>
    <v-col sm="4">
      <div>
        <input name="space" type="radio" /><span> Dining Room</span>
      </div>
    </v-col>
    <v-col sm="4">
      <div>
        <input name="space" type="radio" /><span> Bed Room</span>
      </div>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Step2 extends Vue {
}
</script>

<style lang="scss">
</style>
