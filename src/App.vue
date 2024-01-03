<script setup>
import Header from './components/header.vue'
import Footer from './components/Footer.vue'
import Modal from './components/Modal.vue'
import { ref } from 'vue'

const isOpen = ref (false)

</script>

<template>
    <body>
        <div class="page-wraper">
            <Header @toggleModal="isOpen = !isOpen"/>
        
            <body>
                <main class="main">
                    <router-view></router-view>

                </main>
                <Modal :isOpen="isOpen" @toggleModal="isOpen = !isOpen"/>
            </body>
            

            <Footer />
    </div>
</body>

</template>

<style scoped>
</style>
