<template>
    <div id="skip">
        <a href="#header">헤더 영역</a>
        <a href="#projectInfo" @click="scrollLink($event)">프로젝트 소개 영역</a>
        <a href="#contents__01" @click="scrollLink($event)">콘텐츠 01 영역</a>
        <a href="#contents__02" @click="scrollLink($event)">콘텐츠 02 영역</a>
        <a href="#contents__03" @click="scrollLink($event)">콘텐츠 03 영역</a>
        <a href="#contents__04" @click="scrollLink($event)">콘텐츠 04 영역</a>
        <a href="#contents__05" @click="scrollLink($event)">콘텐츠 05 영역</a>
        <a href="#footer" @click="scrollLink($event)">푸터 영역</a>
    </div>
</template>

<script>
  export default {
      methods: {
          scrollLink(event) {
              event.preventDefault();

              const targetId = event.target.getAttribute("href");
              const targetElement = document.querySelector(targetId);

              if (targetElement) {
                  targetElement.scrollIntoView({ behavior: "smooth" });
              }
          },
      },
  };
</script>