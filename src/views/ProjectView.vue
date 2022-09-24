<script setup lang="ts">
import data from "../assets/project.json"

const projecttData = data;
</script>

<template>

    <div class="project">
        <div v-for="item in projecttData.content">
            <h3 v-if='item.title === "h3"'>
                {{item.text}}
            </h3>
            <div v-if='item.title === "img"' class="imgcontainer">
                <img :src='item.url' width="800" height="450">
            </div>
            <p v-if='item.title === "p"'>
                {{item.text}}
            </p>
        </div>
    </div>




</template>

<style lang="scss" scoped>
.project {
    display: flex;
    flex-direction: column;
    max-width: 1000px;
    margin: 65px auto;

    h3 {
        font-size: 60px;
    }

    p {
        font-size: 30px;
        font-weight: bold;
    }

    .imgcontainer {
        display: flex;
    }

    img {
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    }
}
</style>