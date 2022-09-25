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
                <img :src='item.url' height="450">
            </div>
            <h5 v-if='item.title === "h5"'>
                {{item.text}}
            </h5>
            <p v-if='item.title === "p"'>
                {{item.text}}
            </p>
            <div v-if='item.title === "a"'>
                <a :href='item.url' target="_blank">
                    GitHub連結
                </a>
            </div>
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

    h5 {
        margin: 10px 0px;
        font-size: 45px;
    }

    p {
        margin: 10px 0px 20px 0px;
        font-size: 20px;
    }

    .imgcontainer {
        display: flex;
    }

    img {
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    }
}
</style>