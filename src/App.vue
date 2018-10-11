<template>
    <div class="container">
        <app-header></app-header>
        <hr>
        <div class="row">
        <app-servers></app-servers>
        <app-server-details></app-server-details>
        </div>
        <hr>
        <app-footer></app-footer>
    </div>
</template>

<script>
    import Header from './components/Header.vue';
    import Servers from './components/Servers.vue';
    import ServerDetails from './components/ServerDetails.vue';
    import Footer from './components/Footer.vue';

    export default {
        components: {
            appHeader: Header,
            appServers: Servers,
            appServerDetails: ServerDetails,
            appFooter: Footer
        }
    }

</script>

<style>

</style>
