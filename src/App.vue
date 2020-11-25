<template>
  <div id="app">
    <div id="nav">
      <span class="header">{{ companyName }}</span>
    </div>
      <hr>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    companyName: 'Notridan Tecnologia - Produtos'
  })
}
</script>

<style>
#app {
  font-family: 'Archivo Narrow';
  display: flex;
  flex-direction: column;
}

hr {
  width: 100%;
  color: #a9b4bd;
  border: 1px solid;
}

.header {
  color: #313b42;
  font-size: 33px;
  padding: 10px;
}

#nav {
  padding: 10px;
  text-align: left;
}

</style>
