<script setup>
  import Skip from "@/components/Skip.vue";
  import Header from "@/components/Header.vue";
  import ProjectInfo from "@/components/ProjectInfo.vue";
  import contents_01 from "@/components/contents_01.vue";
</script>

<template>
  <Skip />
  <Header />

  <main id="main" role="main">
    <ProjectInfo />
    <contents_01 />
  </main>

</template>

<style lang="scss">

#main {
  max-width: 1920px;
  position: relative;
}

</style>