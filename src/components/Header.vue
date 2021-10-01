<template>
  <header>
      <div class="logo">
          <img src="../assets/images/logo.png" alt="Logo Molisana">
      </div>
      <nav>
          <ul>
              <li v-for="(link,index) in menu" :key="index"><a :href="link.url" :class="{ active: link.current }" >{{link.text}}</a></li>
          </ul>
      </nav>
  </header>
</template>

<script>
export default {
 name: "Header",
 data() {
    return{
        menu: [
            {
                text: "Home",
                url: "#",
                current: false,
            },
            {
                text: "Prodotti",
                url: "#",
                current: true,
            },
            {
                text: "Chi siamo",
                url: "#",
                current: false,
            },
            {
                text: "Contatti",
                url: "#",
                current: false,
            }
        ]
    }
 }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/variables";
header {
    text-align: center;

    nav {
        margin: 25px 0 ;

        ul {
            display: flex;
            justify-content: center;
            list-style: none;

            a {
                text-decoration: none;
                padding: 20px;
                color: $mainColor;
                font-size: 18px;
                font-weight: 500;
                display: inline-block;

                &.active {
                    background-color: #DBE9FF;
                }
            }   
        } 
    }
}


</style>