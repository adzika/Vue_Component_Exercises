<template>
    <div class="col-xs-12 col-sm-6">
        <p v-if="!server">Please select a server</p>
        <p v-else>Server #{{ server.id }} selected, Status: {{ server.status }}</p>
        <hr>
        <button @click="resetStatus">Change to normal</button>
    </div>
</template>

<script>
    import { serverBus } from "../main.js";

    export default {
        data() {
            return {
                server: null
            }
        },
        name: "ServerDetails",
        methods: {
            resetStatus() {
                this.server.status = 'Normal';
            }
        },
        created() {
            serverBus.$on('selectedServer', (server) => {
                this.server = server;
            });
        }
    }
</script>

<style scoped>

</style>