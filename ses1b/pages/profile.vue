<template>
<section class="container">
<at-steps :current='current'>
  <at-step title="Step1" description="This is a description."></at-step>
  <at-step title="Step2" description="This is a description."></at-step>
  <at-step title="Step3"></at-step>
</at-steps>

<at-button type="primary" @click="previousStep()" style="margin-top: 12px;">Prev</at-button>
<at-button type="primary" @click="nextStep()" style="margin-top: 12px;">Next</at-button>

<nuxt-link to="/homepage"> 
        <at-button size="large"  >Home</at-button>
</nuxt-link>

</section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
  layout: 'blank',
      components: {
    AppLogo
  },
data () {
      return {
        percent: 0,
        current: 0
      }
    },
    methods: {
      descPercent () {
        this.percent -= 10
        this.percent = this.percent < 0 ? 0 : this.percent
      },
      inscPercent () {
        this.percent += 10
        this.percent = this.percent > 100 ? 100 : this.percent
      },
      nextStep() {
        if(this.current < 2) this.current++
      },
      previousStep() {
        if(this.current >0) this.current--
      }
    }

}
</script>

<style scoped>
.container {
  display: 100px; 
  justify-content: center;
  align-items: center;
  text-align: center;
}

.bar {
padding-top: 400px
}


.links {
  padding-top: 15px;
}
</style>


