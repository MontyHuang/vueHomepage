<script setup lang="ts">
import { GithubFilled } from '@ant-design/icons-vue';
</script>

<template>
    <div style="border-top:1px solid #999;background-color:#f1f1f1;">
        <div class="linkToPage">
            <a href="https://github.com/MontyHuang" target="_blank">
                <GithubFilled style="color:#213547;font-size: 50px;" />
                <span>GitHub</span>
            </a>
        </div>
    </div>

</template>

<style lang="scss" scoped>
.linkToPage {
    margin-top: 50px;
    padding-bottom: 50px;
    display: flex;
    justify-content: space-around;
    align-items: center;

    span {
        font-size: 20px;
        display: block;
        color: #213547;
        font-weight: bold;
    }
}

a:link {
    text-decoration: none;
}
</style>
