<template>
    <span class="mySpan">
        <img src="@/assets/logo.png" alt="">
        {{caption}}
    </span>
</template>

<script>
    export default {
        name : "NavLink",


        props: {
            caption : String
        },

        mounted :function () {
            console.log("The link has been created");
            this.testing();
            this.makeRed();
        },


        methods: {
            testing() {
                console.log("The testing method ran on "+this.caption);
            },
            makeRed(){
                if (this.caption == "Google"){
                    this.$el.style.backgroundColor="red";
                }
            }

        },
    }
</script>

<style scoped>
span{
    border : blue solid 2px;
    margin: 10px;
    font-size: 24px;
    font-style: italic;
    background-color: rgb(14, 69, 151);
    color: hotpink;
    border-radius: 20px;
}
img{
    height: 18px;
    background-color: inherit;
}

</style>