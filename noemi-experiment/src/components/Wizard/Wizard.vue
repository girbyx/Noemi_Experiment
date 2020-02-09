<template>
  <v-container fluid>
    <v-row no-gutters>
      <v-col sm="12">
        <h1>{{ header }}</h1>
      </v-col>
    </v-row>
    <v-row no-gutters>
      <v-col class="stepColumn" sm="12">
        <Step1 v-show="currentStep == 1" />
        <Step2 v-show="currentStep == 2" />
        <Step3 v-show="currentStep == 3" />
      </v-col>
      <v-col sm="6">
        <v-btn text small color="primary" v-on:click="goPrev()">Prev</v-btn>
      </v-col>
      <v-col sm="6">
        <v-btn text small color="primary" v-on:click="goNext()">Next</v-btn>
      </v-col>
    </v-row>
    <v-row no-gutters>
      <v-col sm="12">
        <p>Step: {{ currentStep }}/{{ lastStep }}</p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import Step1 from "@/components/Wizard/Steps/Step1.vue";
import Step2 from "@/components/Wizard/Steps/Step2.vue";
import Step3 from "@/components/Wizard/Steps/Step3.vue";

@Component({
  components: {
    Step1,
    Step2,
    Step3
  }
})
export default class Wizard extends Vue {
  @Prop() private header!: string;

  private currentStep = 1;
  private lastStep = 3;
  
  async goNext(){
    if(this.currentStep < this.lastStep){
      this.currentStep++;
    }
  }

  async goPrev(){
    if(this.currentStep > 1){
      this.currentStep--;
    }
  }
}
</script>

<style lang="scss">
button {
  width: 100%;
}

.stepColumn {
  min-height: 500px;
}
</style>
