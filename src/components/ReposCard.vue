<template>
  <div class="bg-white p-8 rounded-xl cursor-pointer" @click="openRepoUrl">
    <div>
      <!-- Usando a tag <img> diretamente e atribuindo a URL da imagem através de uma prop -->
      <img :src="imageUrl" @load="onImageLoad" @error="onImageError" alt="ProjetoFinalMobile" />
      <div v-if="loading" class="loading-placeholder">Carregando...</div>
      <div v-if="error" class="error-placeholder">Erro ao carregar a imagem</div>
    </div>
    <div>
      <h1 class="text-2xl font-semibold">{{ nome }}</h1>
      <p>{{ linguagem }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    nome: String,
    full_name: String,
    linguagem: String,
    html_url: String,
  },
  data() {
    return {
      imageUrl: this.generateImageUrl(),
      loading: true,
      error: false,
    };
  },
  methods: {
    openRepoUrl() {
      if (this.html_url) {
        window.open(this.html_url, "_blank");
      }
    },
    generateImageUrl() {
      return `https://socialify.git.ci/${this.full_name}/image?language=1&owner=1&name=1&stargazers=1&theme=Light`;
    },
    onImageLoad() {
      this.loading = false;
    },
    onImageError() {
      this.loading = false;
      this.error = true;
    },
  },
};
</script>

<style>
.loading-placeholder,
.error-placeholder {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 200px; /* Defina a altura apropriada para a imagem */
  background-color: #f1f1f1; /* Cor de fundo para a área de carregamento ou erro */
  font-size: 16px;
  color: #333;
}
</style>
