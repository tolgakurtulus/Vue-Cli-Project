<template>
  <div class="product">

    <strong>{{ product.title }}</strong>
    <p>{{ product.description }}</p>
    <strong>Price : {{ product.price }}| Pcs : {{ product.count }}</strong>
    <br><br>
    <button @click="addToCart(product)">Add</button>
  </div>
</template>

<script>
export default {

  props : ["product"],
  methods: {
    addToCart(product){
      this.$emit("addToCart", product)
    }
  },
  
}
</script>

<style>

.product{

  border: 2px dashed blueviolet;
  padding: 5px 10px;
  width: 300px;
  height: 125px;
  margin-bottom: 30px;

}

.product:hover{

  border: 2px solid;
  transition: all 1s;
}
  
</style>