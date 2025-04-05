<script lang="ts">
import announcementBar from "@/ui/announcementBar.vue";
export default {
  components: {
    announcementBar,
  },
  methods: {
    scrollIntoView() {
      document
        .getElementById("pageIntro")
        ?.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>
<template>
  <div
    class="flex flex-col h-screen justify-between overflow-hidden"
  >
    <div class="relative h-screen">
      <div
        class="w-screen max-w-2xl absolute inset-0 filter backdrop-blur-md rounded-xl"
      >
        <div class="mx-20 flex-col">
          <img src="/logo.svg" class="h-80 mt-36 max-xl:mt-24" />
          <p class="mt-16 mb-36 text-3xl text-gray-100 dark:text-slate-100 font-bold">
            Forge Alchemy, Sculpt Epochs.
          </p>
          <div class="md:flex md:items-center mt-6">
            <a href="https://github.com/csaslu" class="ml-5">
              <img
                src="/Github.svg"
                class="h-16 max-sm:mt-4 invert dark:filter dark:invert"
              />
            </a>
          </div>
        </div>
      </div>
      <div class="fixed inset-0 -z-50">
        <div
          class="dark:w-full dark:h-full dark:absolute dark:inset-0 dark:bg-black dark:opacity-30"
        ></div>
        <video class="object-cover w-full h-full" autoplay muted loop>
          <source src="/lida.mp4" type="video/mp4" />
        </video>
      </div>
    </div>
  </div>
  <announcementBar>
    <a class="text-white">🎉我们正在招新！</a>
    <a
        href="javascript:void(0)"
        @click="scrollIntoView"
        class="text-white nounderline hover:underline"
    >
      <b>点击这里查看详情 →</b>
    </a>
  </announcementBar>
</template>
