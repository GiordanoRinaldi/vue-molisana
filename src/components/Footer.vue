<template>
  <footer>

      <div class="logo">
          <img src="../assets/images/logo.png" alt="Logo Molisana">
      </div>
      <div class="link-footer">
        <div class="link-pastificio">
          <h3>PASTIFICIO</h3>
          <ul>
            <li v-for="(link,index) in pastificio" :key="index"><a href="#">{{link}}</a></li>
          </ul>
        </div>
        <div class="link-prodotti">
          <h3>PRODOTTI</h3> 
          <ul>
            <li v-for="(link,index) in prodotti" :key="index"><a href="#">{{link}}</a></li>
          </ul>
        </div>
      </div>
  </footer>
</template>

<script>
export default {
 name: "Footer",
 data(){
   return{
     pastificio: ["Il Pastificio", "Grano", "Filiera", "100 anni di pasta", "Sartoria della pasta", ],
     prodotti: ["Le classiche", "Le Integrali", "Le Speciali", "Le Biologiche", "Le Gluten-free", ]
   }
 }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/variables";

  footer{
    display: flex;
    height: 400px;
    width: 1200px;
    margin: 0 auto;
    padding-top: 40px;
    background-image: url('../assets/images/footer.jpg');
    background-repeat: no-repeat;
    background-position-y: bottom;
  }

  .logo{
    display: inline-block;
    margin-right: 130px;
  }

  .link-footer{
    display: flex;
    .link-pastificio {
      margin-right: 250px;
    }
  }

  h3{
    margin-bottom: 25px;
    color: $mainColor;
  }

  ul{
    list-style: none;
    line-height: 25px;
    a{
      text-decoration: none;
      color: black;
      
    }
  }
</style>