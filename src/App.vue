<template>
    <v-app class="bg">
        <v-main>
            <MainPage />
        </v-main>
    </v-app>
</template>

<script>
import MainPage from './components/MainPage.vue'


export default {
    name: 'App',

    components: {
        MainPage,
    },
}
</script>

<style src="./App.css"/>