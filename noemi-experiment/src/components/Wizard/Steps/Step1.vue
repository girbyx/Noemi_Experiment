<template>
  <v-row>
    <v-col sm="12">
      <h1>What colors you like?</h1>
    </v-col>
    <v-col sm="4">
      <div>
        <input name="color" type="radio" /><span> Red</span>
      </div>
      <div class="color red"></div>
    </v-col>
    <v-col sm="4">
      <div>
        <input name="color" type="radio" /><span> Blue</span>
      </div>
      <div class="color blue"></div>
    </v-col>
    <v-col sm="4">
      <div>
        <input name="color" type="radio" /><span> Yellow</span>
      </div>
      <div class="color yellow"></div>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Step1 extends Vue {
}
</script>

<style lang="scss">
.color {
  width: 100%;
  height: 100px;
  
  &.red {
    background: red;
  }

  &.blue {
    background: blue;
  }

  &.yellow {
    background: yellow;
  }
}

</style>
