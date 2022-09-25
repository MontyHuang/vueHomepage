<script setup lang="ts">
import { GithubFilled } from '@ant-design/icons-vue';
</script>

<template>
  <div class="container">
    <div class="lefspace"></div>
    <div class="introduce">
      <h1>
        Hello, there! I'm Monty Huang.
      </h1>
      <p>
        這是我透過
        <span>
          Vue3 + Vite + Vue-Router
        </span>
        所建構的個人網站.
        <br />
        <div class="link">
          <a href="https://github.com/MontyHuang" target="_blank">
          <GithubFilled style="color:#213547;font-size: 70px;" />
        </a>
        </div>

      </p>
    </div>

  </div>

</template>

<style lang="scss" scoped>
.container {
  display: flex;
  width: 100%;
  height: 100vh;
  background: linear-gradient(250deg, white 50%, transparent 0%) center center / 100% 100%,
    url("../assets/coding.jpg") left center / auto 100%;
}
.lefspace{
  display: flex;
  flex:1.2;
}
.introduce {
  // margin: 0px 0px 0px 850px;
  height: 100%;
  display: flex;
  flex:1;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  font-weight: bold;

  h1 {
    font-size: 40px;
  }

  span {
    font-size: 30px;
    background: -webkit-linear-gradient(315deg, #42d392 25%, #647eff);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  p {
    font-size: 20px;
  }
}
.link{
  margin-top: 50px;
  display: flex;
  justify-content: center;
}
</style>
