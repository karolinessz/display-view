<template>
  <div class="products">
    <table>
      <tr>
        <th v-for="title in titles" v-bind:key="title.index"> {{ title }} </th>
      </tr>
      <tr v-for="product in products" v-bind:key="product.index">
        <td>{{ product.id }}</td>
        <td>{{ product.date }}</td>
        <td>{{ product.name }}</td>
        <td>{{ product.price }}</td>
        <td><i class="material-icons">create</i></td>
        <td><i class="material-icons">clear</i></td>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: 'Products',
  data: () => ({
    titles: [
      'ID',
      'Data da Criação',
      'Nome',
      'Preço',
      'Editar',
      'Excluir'
    ],
    products: [
      {
        id: 234,
        date: '23/11/2020',
        name: 'Cadeira',
        price: '25,40'
      },
      {
        id: 257,
        date: '24/11/2020',
        name: 'Mesa',
        price: '120,50'
      },
      {
        id: 247,
        date: '24/11/2020',
        name: 'Cadeira',
        price: '234,50'
      },
      {
        id: 454,
        date: '22/11/2020',
        name: 'Copo',
        price: '0,34'
      },
      {
        id: 284,
        date: '22/11/2020',
        name: 'Notebook',
        price: '1134,40'
      },
      {
        id: 781,
        date: '22/11/2020',
        name: 'Notebook',
        price: '1946,50'
      },
      {
        id: 268,
        date: '22/11/2020',
        name: 'Notebook',
        price: '2734,00'
      },
      {
        id: 531,
        date: '21/11/2020',
        name: 'Notebook',
        price: '3458,00'
      },
      {
        id: 890,
        date: '21/11/2020',
        name: 'Cadeira',
        price: '25,40'
      },
      {
        id: 876,
        date: '21/11/2020',
        name: 'Cadeira',
        price: '25,40'
      },
      {
        id: 467,
        date: '21/11/2020',
        name: 'Mesa',
        price: '120,50'
      }
    ],
  })
}
</script>

<style>
table, td, th {
  border: 2px solid #9dadba;
  color: #313b42;
}

td {
  padding: 2px;
}

table {
  text-align: center;
  padding: 2px;
  width: 100%;
  border-collapse: collapse;
}

.products {
  text-align: center;
}

.material-icons {
  font-size: 35px;
}

th {
  padding: 5px;
}

i {
  border: 0px;
  background: white;
  color: #313b42;
  cursor: pointer;
  padding: 5px;
}
</style>
