<script setup>
  import Skip from "@/components/Skip.vue";
  import Header from "@/components/Header.vue";
  import ProjectInfo from "@/components/ProjectInfo.vue";
  import ProjectInfo2 from "@/components/ProjectInfo2.vue";
</script>

<template>
  <Skip />
  <Header />

  <main id="main" role="main">
    <ProjectInfo />
    <ProjectInfo2 />
  </main>

</template>

<style lang="scss">

#main {
  max-width: 1920px;
  overflow: hidden;
  margin: 0 auto;
  position: relative;
}

</style>