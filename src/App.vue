<template>
  <div class="box">
    <header>
      <h1>hello</h1>
    </header>
    <main>
      <router-view></router-view>
    </main>
    <footer>
      <router-link to="/">首页</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/taik">父子组件通讯</router-link>

    </footer>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
html,
body,
#app {
  width: 100%;
  height: 100%;
}
.box {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
main {
  flex: 1;
  overflow: auto;
}
header {
  width: 100%;
  height: 50px;
}

footer {
  width: 100%;
  height: 50px;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
</style>
