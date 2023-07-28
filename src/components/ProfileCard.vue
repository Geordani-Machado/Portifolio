
<template>
    <div>
      <div>
          <div class="flex">
            <img src="https://avatars.githubusercontent.com/u/74798854?v=4" class="rounded-full md:h-72 h-24"/>
            <div class="ml-12">
              <h1 class="font-bold md:text-4xl">Geordani Machado</h1>
              <p>FullStack developer Pleno at Ânima Educação</p>
              <Skils class="hidden md:block"/>
            </div>
          </div>
          <Skils class="block md:hidden"/>
      </div>
    </div>
</template>

<script setup>
import Skils from './Skils.vue';
</script>