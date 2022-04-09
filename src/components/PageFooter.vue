<template>
    <div>
        © All rights reserved
        <nav>
            <NavLink :caption="'Google'"/>
            <!-- <a href="https://google.ca">Google</a> -->
        </nav>
    </div>
</template>

<script>
import NavLink from './NavLink.vue'
    export default {
        name : 'PageFooter',
        components: {
            NavLink,
        },
    }
</script>

<style scoped>
nav a{
        color : hotpink;
    }


</style>