<template>
    <div>
        <h1>{{ greeting }} {{ myNum }}</h1>
        {{ secondNum }}
        {{ secondMessage }}
        <nav>
            <NavLink caption="VueJS docs"/>
            <NavLink caption="Google"/>
            <NavLink caption="DevDocs"/>

            <!-- <a href="https://v2.vuejs.org" target="_blank">Vue 2 docs</a>
            <a href="https://google.ca" target="_blank">Google</a>
            <a href="https://devdocs.io" target="_blank">devdocs</a> -->
        </nav>

    </div>
</template>

<script>
import NavLink from './NavLink.vue';

    export default {
        name : "PageHeader",
        components: {
            NavLink
        },
        props: {
            myNum : Number,
            greeting : {
                type : String,
                validator : function(val){
                    if (val.length < 5){
                        console.warn("The greeting must be longer than 5 characters");
                        return false;
                    }
                    return true;
                }
            }
        },
        data() {
            return {
                secondNum: 12,
                secondMessage : "Hello again"
            }
        },
        methods: {
            makeRed : function() {
                document.body.style.backgroundColor="red";
            },
            makeBlue(){
                document.body.style.backgroundColor="blue";
            }
        },
    }
</script>

<style scoped>
a{
    margin-right: 10px;
}

</style>