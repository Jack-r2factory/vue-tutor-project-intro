<template>
    <v-footer absolute bottom padless width="100%" id="footer">
        <v-toolbar-title id="footer-title">{{ new Date().getFullYear() }} — <strong>Footer</strong></v-toolbar-title>
    </v-footer>
</template>



<style>
    #footer {
        background-color: #0083cb;
    }

    #footer-title {
        color: white;
        text-align: center;
    }
</style>
