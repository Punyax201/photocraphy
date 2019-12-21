<template>
    <div class="wrapper primary" :class="btnMode ? 'toggleBtnOn':'toggleBtnOff'" v-on:click="btnMode = !btnMode">
        <div class="inner-wrapper accent">
            <p v-if="btnMode" :style="{'position':'static','transform':'translate(30px,15px)','cursor':'pointer'}">
                GRID
            </p>
        </div>
            <p v-if="!btnMode" :style="{'position':'static','transform':'translate(15px,10px)','cursor':'pointer'}">
                TIMELINE
            </p>
    </div>
</template>
<script>
/* eslint-disable */
export default {
    data(){
        return{
            btnMode: true
        }
    },
    methods: {
        toggle: function() {
            console.log("a");
            this.btnMode = !this.btnMode;
        }
    }
}
</script>
<style scoped>
    .wrapper{
        overflow: hidden;
        height: 100px;
        width: 100px;
        border-radius: 50%;
        box-sizing: content-box;
        padding: 0px;
    }
    .inner-wrapper{
        padding: 0px;
        height: 50px;
        content: 'as';
    }

    .toggleBtnOn{
        animation: toggleOn 0.2s 1;
    }
    .toggleBtnOff{
        animation: toggleOff 0.2s 1;
    }

    @keyframes toggleOn {
        100%{
            transform: rotateZ(360deg);
        }
    }
    @keyframes toggleOff {
        100%{
            transform: rotateZ(-360deg);
        }
    }
</style>
