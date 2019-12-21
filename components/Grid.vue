<template>
    <v-container>
    <v-btn @click="gridCols=12">Kedar kantha</v-btn>
    <v-btn @click="gridCols=12">Deo Tibba</v-btn>
        <v-row>
            <v-col :cols="gridCols" v-for="i in im1" :key="i" :style="{'transition':'width 2s'}">
                <v-card>
                    <v-card-title>{{ i.title }}</v-card-title>
                    <v-card-text>
                        <img class="image" :src="i.url">
                    </v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>
<script>
/* eslint-disable */
export default {
    data(){
        return {
            gridCols:6,
            im1: this.$store.state.imageData.images
        }
    }
}
</script>
<style scoped>
    .image{
        width: 100%;
        height: auto;
    }
</style>
