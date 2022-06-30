<template>
    <div id="about-container">
        <p class="main-subheading">{{ message }}</p>
        <p>{{ message2 }}</p>
    </div>
    <div id="img-container">
        <img id="r2-factory-logo" alt="R2 Factory Logo" src="https://pbs.twimg.com/profile_images/1526834705823416320/bcPzQTAu_400x400.jpg"/>
    </div>
</template>

<script>
    export default {
        data() {
            return {
            message: 'This text is inside a javascript script tag!',
            message2: 'This text is also inside the same script tag as a different variable'
            }
        }
    }
</script>

<style>
    #about-container {
        text-align: center;
    }

    .main-subheading {
        font-size: 1.5rem;
    }

    p {
        color: #0083cb;
    }

    #img-container {
        display: flex;
        justify-content: center;
    }

    #r2-factory-logo {
        margin-top: 15px;
    }
</style>