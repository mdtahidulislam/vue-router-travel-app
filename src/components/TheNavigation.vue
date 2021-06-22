<template>
  <div id="nav">
    <router-link to="/">Home</router-link>
    <router-link to="/brazil">Brazil</router-link>
    <router-link to="/jamaica">Jamaica</router-link>
    <router-link to="/hawaii">Hawaii</router-link>
    <router-link to="/panama">Panama</router-link>
  </div>
</template>

<style scoped lang="css">
    #nav .active-link {
        color: #44BA81;
        border-bottom: 1px solid #44BA81;
    }
</style>