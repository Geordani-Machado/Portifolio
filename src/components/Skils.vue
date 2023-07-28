<template>
    <div class="justify-center">
          <div class="md:mt-12">
            <div class="grid md:grid-cols-10 grid-cols-10 gap-1">
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/vue.js" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/tailwindcss" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/redis" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/vitess" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/react" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/electron" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/Mysql" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/.NET" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/JavaScript" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/TypeScript" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/Node.js" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/postgresql" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/amazonaws" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/firebase" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/mongodb" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/yarn" />
              <img class="p-1" height="40" width="40" src="https://cdn.simpleicons.org/visualstudiocode" />
            </div>
              <div class="flex md:mt-12 cursor-pointer" @click="openLinkedInProfile">
              <img height="32" width="32" src="https://cdn.simpleicons.org/linkedin" />
              <p class="ml-2 font-semibold">Geordani-Machado</p>
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