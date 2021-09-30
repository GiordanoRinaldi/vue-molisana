<template>
  <section>
    <h2>Lista Prodotti</h2>
    <div class="prodotti">
      <div v-for="(pasta, index) in paste" :key="index" class="prodotto">
        <img :src="require('@/assets/images/paste/'+ pasta.img)" :alt="pasta.nome">
        <h3>{{pasta.nome}}</h3>
      </div>
    </div>
  </section>
</template>

<script>
export default {
 name: "Products",
 data(){
   return{
     paste:[
       {
        nome: "N.4 Spaghetto Quadrato Bucato",
        img: "1.jpg",
       },
       {
        nome: "N.5 Fettuccine",
        img: "2.jpg",
       },
       {
        nome: "N.6 Linguine",
        img: "6.jpg",
       },
       {
        nome: "N.7 Mezze Linguine",
        img: "7.jpg",
       },
       {
        nome: "N.11 Spaghettino Quadrato",
        img: "11.jpg",
       },
       {
        nome: "N.38 Mezze maniche",
        img: "38.jpg",
       },
       {
        nome: "N.44 Sedani",
        img: "44.jpg",
       },
       {
        nome: "N.49 Sedanini",
        img: "49.jpg",
       },
       {
        nome: "N.53 Lumachine",
        img: "53.jpg",
       },
       {
        nome: "N.55 Chifferi rigati",
        img: "55.jpg",
       },
       {
        nome: "N.58 Misto corto",
        img: "58.jpg",
       },
       {
        nome: "N.84 Ditale Quadrato",
        img: "84.jpg",
       }
     ]
   }
 }
}
</script>

<style lang="scss" scoped>
  @import "@/assets/style/common";
  @import "../assets/style/variables";
  section {
    background-image: url('~@/assets/images/bg-prods.jpg');
  }

  .prodotti{
    width: 1200px;
    margin: auto;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    
    padding-bottom: 60px;

    .prodotto{
      width: calc(100% / 4);
      background-color: white;
      border: 4px solid #dbe9ff;
      img {
        width: 100%;
      }
    }
  }


  h3, h2{
    text-align: center;
    color: $mainColor;
  }

  h2{
    padding: 50px 0  40px 0;
  }

</style>