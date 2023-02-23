<script setup>

import Events from "@/components/Events.vue";
</script>

<template>
    <header>


      <div class="wrapper">
           Menu
      </div>
    </header>

    <main>
            <Events/>
    </main>
      <footer>
        Footer
      </footer>

</template>

<style scoped>

header {
  line-height: 1.5;
  background-color: #8bbdbb;
  color: white;
  flex : 1
}
main {
  flex : 15
}
footer {
  flex : 1;
  background-color: darkgrey;

}


</style>
