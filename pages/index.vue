<template>
  <div>
    <div class="w-container">
      <div class="card">
        <h1 class="heading">Accueil </h1>
        <p>Par Nicolas Reszka</p>
        <a v-show="showButton" href="#" class="button w-button" @click="hideButton()">Clique et je disparais</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  layout: "default",
  data() {
    return {
      showButton: true
    }
  },
  methods: {
    hideButton() {
      this.showButton = false;
    }
  }
}
</script>

