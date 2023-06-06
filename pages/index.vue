
<script setup>


    const { $notion } = useNuxtApp()

    const { data } = await useAsyncData("notion", () => $notion.getPageBlocks("ee2cd38c7a10448aad8b5b8c83c763e0"))
    
</script>

<template>
    <div class="app">
    <div class="wrapper">
      <Menu />
      <main class="main">
        <NotionRenderer :blockMap="data" fullPage prism />

        
      </main>
    </div>
  </div>
</template>


<style lang="sass" scoped>
  .app
    @apply min-h-full max-w-full bg-slate-100
    .wrapper
        @apply grid grid-cols-[300px_1fr]
     </style>