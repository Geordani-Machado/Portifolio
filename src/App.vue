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
  <div class="bg-zinc-100 w-full-max h-full-max p-32">
    <ProfileCard class=""/>
    <div class="grid grid-cols-3 gap-8 px-48 py-12">
      <ReposCard v-for="repo in publicRepos" :key="repo.name" :nome="repo.name" :linguage="repo.language" :html_url="repo.html_url" :full_name="repo.full_name" />
    </div>
  </div>
</template>

