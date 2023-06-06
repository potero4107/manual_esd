<script setup>
import Logo from './logo.vue';
</script>

<template>
    <aside class="sidebar">
        <div class="side_wrapper">
            <div class="logo">
                <div class="svg">

                    <div class="first_level">

                        <NuxtLink to="/">
                            <Logo />
                        </NuxtLink>

                    </div>
                </div>
            </div>
            <div class="navigation">
                <div class="first_level">

                    <NuxtLink to="/styles">Estilos</NuxtLink>

                </div>
                <div class="first_level">

                    <NuxtLink to="/buttons">Botones y chips</NuxtLink>

                </div>
                <div class="first_level">

                    <NuxtLink to="/cards">Cards</NuxtLink>

                </div>
                <div class="first_level">

                    <NuxtLink to="/avatars">Avatares y burbujas</NuxtLink>

                </div>
                <div class="first_level">

                    <NuxtLink to="/lists">Listas y dropdowns</NuxtLink>

                </div>
                <div class="first_level">

                    <NuxtLink to="/inputs">Inputs</NuxtLink>

                </div>
                <div class="first_level">

                    <NuxtLink to="/misc">Miscelánea</NuxtLink>

                </div>

            </div>
        </div>
    </aside>
</template>

<style lang="sass" scoped>
.sidebar
    @apply bg-slate-100 col-start-1 col-end-2 top-0 min-h-screen flex items-start
    .side_wrapper
        @apply overflow-auto top-0 sticky w-full
        .logo
            @apply bg-yellow-300 flex px-5 items-center h-[60px]
            &:hover
                @apply bg-yellow-200
            

        .navigation
            @apply p-4 flex flex-col m-2 divide-y divide-slate-300
            .first_level
                @apply text-slate-600 font-semibold py-2
                &:hover
                    @apply text-slate-900


</style>