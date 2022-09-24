<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue'
import { computed } from "@vue/reactivity";
import { CodeFilled } from '@ant-design/icons-vue';


//state
const navbar = [{title:"Home",path:"./"},{title:"About",path:"./about"},{title:"Project",path:"./project"}]
const name = ref("Monty Huang");

// Computed props
const nameFornav = computed(()=>{
  return name.value;
})

</script>

<template>

  <header class="navbar">
    <code-filled style="color:#213547;font-size: 30px;padding-right: 10px;" />
    <span class="title">{{nameFornav}}</span>
    <div class="navbar-right">
      <li v-for="item in navbar">
        <RouterLink :to={path:item.path}>{{item.title}}</RouterLink>
      </li>
    </div>
  </header>
  <RouterView />

</template>

<style scoped>
.navbar {
  position: fixed;
  display: flex;
  align-items: center;
  top: 0;
  padding: 10px 0px 10px 20px;
  width: 100%;
  box-shadow:1px 1px 5px rgba(0, 0, 0, 0.19);
  background-color: white;
}

.navbar-right {
  font-size: 20px;
  font-weight: 900;
  color: #213547;
  margin-left: auto;
  display: flex;
  justify-content: flex-end;
}

.title {
  font-size: 30px;
  font-weight: 900;
  color: #213547;
}

a {
  position: relative;
  color: #213547;
  margin-right: 50px;
}

a:link {
  text-decoration: none;
}

a:after {
  content: '';
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 3px;
  bottom: 0;
  left: 0;
  background-color: #213547;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

a:hover {
  color: #213547;
}

a:hover:after {
  transform: scaleX(1);
  transform-origin: bottom left;
}
</style>
