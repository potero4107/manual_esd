
<script setup>


    const { $notion } = useNuxtApp()

    const { data } = await useAsyncData("notion", () => $notion.getPageBlocks("74562341dad843f2972000a442da1646"))
    
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
    @apply min-h-full max-w-full 
    .wrapper
        @apply grid grid-cols-[300px_1fr]
     </style>