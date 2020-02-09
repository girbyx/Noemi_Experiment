<template>
  <div>
    <h1>{{ header }}</h1>
    <Step1 v-show="currentStep==1" class="step" />
    <Step2 v-show="currentStep==2" class="step" />
    <Step3 v-show="currentStep==3" class="step" />
    <button v-on:click="goPrev()" class="prevButton">Prev</button>
    <button v-on:click="goNext()" class="nextButton">Next</button>
    <p>Step: {{ currentStep }}/{{ lastStep }}</p>
  </div>
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
  &.prevButton{

  }

  &.nextButton{

  }
}

.step {
  
}
</style>
