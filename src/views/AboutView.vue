<script setup lang="ts">
import { UserOutlined } from '@ant-design/icons-vue';
import data from '../assets/about.json'

const aboutData = data;

</script>

<template>
  <div class="about">
    <div class="card">
      <div class="user">
        <div class="userImg">
          <span class="tooltiptext">{{aboutData.tooltiptext}}</span>
          <UserOutlined style="color:#213547;font-size: 70px;" />
        </div>
      </div>
      <h2>ABOUT ME</h2>
      <h3 >{{aboutData.text.h3}}</h3>
      <p>
        {{aboutData.text.textinline[0].p}}
      </p>
      <p style="padding-top:20px ;word-spacing: 5px">
        {{aboutData.text.textinline[1].p}}
      </p>

    </div>
  </div>

</template>

<style lang="scss" scoped>
.about {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background-color: #bacad9;
}

.card {
  margin-top: 65px;
  width: 500px;
  height: 500px;
  border-radius: 30px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.3s;
  background-color: white;

}

.user {
  padding-top: 50px;
  display: flex;
  justify-content: center;

  .userImg {
    border-radius: 50%;
    width: 100px;
    height: 100px;
    background-color: #d3d3d3;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;

    .tooltiptext {
      visibility: hidden;
      width: 200px;
      background-color: gainsboro;
      color: #213547;
      text-align: center;
      border-radius: 6px;
      padding: 5px 0;
      font-weight: bold;

      /* Position the tooltip */
      position: absolute;
      z-index: 1;
    }
  }
}

.userImg:hover .tooltiptext {
  visibility: visible;
  left: 105%;
}


h2 {
  display: flex;
  justify-content: center;
  font-size: 30px;
  font-weight: 900;
}

h3 {
  display: flex;
  justify-content: center;
  font-size: 20px;
  font-weight: 900;
  color: #213547;
}

p {
  display: flex;
  justify-content: center;
  font-size: 15px;
  color: #213547;
}
</style>
