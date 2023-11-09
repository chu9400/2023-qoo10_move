<script setup>
  import Skip from "@/components/Skip.vue";
  import Header from "@/components/Header.vue";
  import ProjectInfo from "@/components/ProjectInfo.vue";
  import contents_01 from "@/components/contents_01.vue";
  import contents_02 from "@/components/contents_02.vue";
  import contents_03 from "@/components/contents_03.vue";
  import contents_04 from "@/components/contents_04.vue";
  import contents_05 from "@/components/contents_05.vue";
  import Footer from "@/components/Footer.vue";
</script>

<template>
  
  <Skip />
  <Header />

  <main id="main" role="main">
    <ProjectInfo /> 
    <contents_01 />
    <contents_02 />
    <contents_03 />
    <contents_04 />
    <contents_05 />
  </main>

  <Footer />

</template>

<style lang="scss">

#main {
  max-width: 1920px;
  position: relative;
  overflow: hidden;
}

</style>