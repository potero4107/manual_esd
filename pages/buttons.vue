
<script setup>


    const { $notion } = useNuxtApp()

    const { data } = await useAsyncData("notion", () => $notion.getPageBlocks("5c7842c3215a430c80626a574b77cb0b"))
    
</script>

<template>
    <div class="app">
    <div class="wrapper">
      <Menu />
      <main class="main">
        <NotionRenderer :blockMap="data" fullPage prism/>

        
      </main>
    </div>
  </div>
</template>


<style lang="sass" scoped>
  .app
    @apply min-h-full max-w-full 
    .wrapper
        @apply grid grid-cols-[300px_1fr]
     </style>