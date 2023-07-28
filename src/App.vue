<script setup>
import ProfileCard from './components/ProfileCard.vue';
import ReposCard from "./components/ReposCard.vue"
</script>

<script>
export default {
  data() {
    return {
      publicRepos: [] // Armazenará os repositórios públicos obtidos da API
    };
  },
  created() {
    this.fetchRepos(); // Chamada da função para buscar os repositórios
  },
  methods: {
    async fetchRepos() {
      try {
        const response = await fetch("https://api.github.com/users/Geordani-Machado/repos");
        const data = await response.json();
        this.publicRepos = data.filter(repo => repo.visibility === "public");
      } catch (error) {
        console.error("Erro ao buscar os repositórios:", error);
      }
    }
  }
};
</script>

<template>
  <div class="bg-zinc-100 w-full-max h-full-max md:p-32 p-7">
    <ProfileCard class="md:px-48 p-8"/>
    <div class="grid md:grid-cols-3 sm:grid-cols-1 gap-8 md:px-48 py-12">
      <ReposCard v-for="(repo, index) in publicRepos" :key="repo.name" :nome="repo.name" :linguagem="repo.language" :html_url="repo.html_url" :full_name="repo.full_name" :class="{ 'loading-animation': isLoading }" :style="{ 'animation-delay': index * 0.2 + 's' }" />
    </div>
    <div>
      <h1 class="text-center">Projeto desenvolvido com muito ❤️☕ Por Geordani Machado junto com a Turma de TI do Discord da Ânima Educação</h1>
    </div>
  </div>
</template>



