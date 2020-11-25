<template>
  <div class="home">
    <div class="actions">
      <div class="filter">
      <span style="font-size:20px;padding: 15px 0px;">Nome:</span>
      <input type="text" class="filter-input" placeholder="Nome">
      </div>
      <button class="add">Novo Produto</button>
    </div>
    <Products />
    <div class="pages">
      <button class="page" v-for="page in numberPages" v-bind:key="page.index"> {{ page }} </button>
    </div>
  </div>
</template>

<script>
import Products from '@/components/Products.vue'

export default {
  name: 'Home',
  components: {
    Products
  },
  data: () => ({
    numberPages: [
      1,
      2,
      3
    ]
  })
}
</script>

<style >
.home {
  align-content: center;
  display: flex;
  flex-direction: column;
  padding: 0px 60px;
  font-size: 22px;
}

.actions {
  padding: 60px 0px;
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  justify-content: space-between;
}

.filter-input {
  font-size: 20px;
  height: 36px;
  padding: 5px;
}

.add {
  font-family: 'Archivo Narrow';
  background-color: #6658f5;
  min-height: 50px;
  width: 15%;
  color: white;
  border: 0px;
  border-radius: 5px;
  font-size: 25px;
  cursor: pointer;
}

.page {
  font-family: 'Archivo Narrow';
  background-color: #6658f5;
  min-height: 50px;
  min-width: 5%;
  color: white;
  font-size: 27px;
  border: 0px;
  border-radius: 5px;
  margin: 5px;
  cursor: pointer;
}

.pages {
  padding: 40px;
  display: flex;
  justify-content: center;
}

.filter {
  display: flex;
  flex-direction: column;
}

</style>