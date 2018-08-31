<template>
<section class="container">
<at-progress :percent="percent" class="bar"></at-progress>
<at-button-group size="small" class="links" >
  <at-button @click="descPercent"><i class="icon icon-chevron-left"></i></at-button>
  <at-button @click="inscPercent"><i class="icon icon-chevron-right"></i></at-button>
</at-button-group>

</section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
      components: {
    AppLogo
  },
data () {
      return {
        percent: 0
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

.textContainer {
padding-top: 10px
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 30px;
  color: #35495e;
  letter-spacing: 1px;
}


.links {
  padding-top: 15px;
}
</style>


