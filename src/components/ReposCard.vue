<template>
    <div class="bg-white p-8 rounded-xl cursor-pointer"  @click="openRepoUrl">
      <div>
        <img :src="generateImageUrl()" alt="ProjetoFinalMobile" width="640" height="320" />
      </div>
      <div>
        <h1 class="text-2xl font-semibold">{{nome}}</h1>
        <p>{{ linguage }}</p>
      </div>
        
    </div>
</template>

<script>
export default {
  props: {
    nome: String,
    full_name: String, 
    linguage: String,
    html_url: String
  },
  methods: {
    openRepoUrl() {
      if (this.html_url) {
        window.open(this.html_url, "_blank");
      }
    },
    generateImageUrl() {
      return `https://socialify.git.ci/${this.full_name}/image?language=1&owner=1&name=1&stargazers=1&theme=Light`;
    }
  }
};
</script>