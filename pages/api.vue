<template>
    <div>
        <div class="w-container">
            <div class="card">
                <h1 class="heading">Exemple d&#x27;appel API</h1>
                <p>Depuis <a href="#">https://jsonplaceholder.typicode.com</a>
                </p>
                <a href="#" class="button w-button" @click="getPosts()">Lancer !</a>
            </div>
        </div>
        <div>
            <div class="w-container">
                <div v-for="post in data" :key="post.id" class="card">
                    <h1 class="heading">{{post.title}}</h1>
                    <p class="paragraph">{{post.body}}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  layout: "default",
  data() {
    return {
      data: []
    }
  },
  methods: {
    getPosts() {
        this.$axios
            .$get(`https://jsonplaceholder.typicode.com/posts`)
            .then(data =>  {
                this.data = data;
                console.log(data);
            })
            .catch(error => {
                console.error(error);
            })
    }
  }
}
</script>
