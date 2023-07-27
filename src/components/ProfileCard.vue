
<template>
    <div>
      <div class="flex">
        <img src="https://avatars.githubusercontent.com/u/74798854?v=4" class="rounded-full w-72"/>
        <div class="justify-center mt-16 ml-12">
          <h1 class="font-bold text-4xl">Geordani Machado</h1>
          <p>FullStack developer Pleno at Ânima Educação</p>

          <div class="flex mt-12">
            <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/vue.js" />
            <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/Mysql" />
            <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/.NET" />
            <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/JavaScript" />
            <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/TypeScript" />
            <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/Node.js" />
            <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/postgresql" />
            <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/amazonaws" />

          <div class="flex ml-32 cursor-pointer" @click="openLinkedInProfile">
          <img height="32" width="32" src="https://cdn.simpleicons.org/linkedin" />
          <p class="ml-2 font-semibold mt-2">Geordani-Machado</p>
        </div>
          </div>

          
        </div>

      </div>
    </div>
</template>

<script>
export default {
    methods: {
        openLinkedInProfile() {
            window.open("https://www.linkedin.com/in/geordani-machado/", "_blank");
        }
    }
};
</script>