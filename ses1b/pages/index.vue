<template>
  <section class="container">
    <div>
      <app-logo/>
      <!-- <h1 class="title">
      </h1> -->
      <!-- <h2 class="subtitle">
        doing this to carry the boys in ses1b
      </h2> -->
        <section class="textContainer">
        <at-input v-model="inputValue" placeholder="hey"></at-input> 
        </section>
        <section class="textContainer">
        <at-input v-model="password" type="password" placeholder="Password"></at-input>
        </section>
      <div class="links">
        <router-link to="/profile"> 
        <at-button size="large"  >Login</at-button>
        </router-link>
      </div>
    </div>
    
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
  components: {
    AppLogo
  }
}
</script>

<style>
.container {
  min-height: 70vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
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

/* .subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
} */

.links {
  padding-top: 15px;
}
</style>

