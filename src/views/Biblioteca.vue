<script setup>
import Footer from "@/components/Footer.vue";
import Menu from "@/components/Menu.vue";
import MenuMobile from "@/components/MenuMobile.vue";
import BookInfo from "@/components/BookInfo.vue";
</script>



<template>
  <div v-if="!isMobile()" class="marginMenu">
    <Menu
      :plotDropDown="true"
      :filter="filterDropdown"
      :actualCategory="$route.query.category"
    />
  </div>

  <div v-else>
    <MenuMobile
    :plotDropDown="true"></MenuMobile>
  </div>

  <div class="page-title">
   <p> Seus Ebooks </p>
  </div>

  <div class="grid-conteiner">

  <div class="book-grid">

  <div v-for="book in book_details" >
    
    <BookInfo
        :name="book.name"  
        :author="book.author"
        :filename = "book.img"
        class = book
    />
  </div>
    </div>
     </div>
  <Footer></Footer>
  
</template>

<script>
export default {
  name: 'app',
  methods:{
    isMobile() {
      if(window.screen.availWidth < 700){
        return true
        } else {
        return false
        }
        }
    },
  data () {
    return {
      book_details:[
        {
          name: "Harry Potter e a pedra filosofal",     
          img: "/assets/0.2516068b.jpg",
          author: "JK Rowling"
                },
                {
          name: "Eragon",     
          img: "/assets/1.e7281dd3.jpg",
          author: "Christopher Paolini"
                },
                {
          name: "Crepúsculo",     
          img: "/assets/2.373fc438.jpg",
          author: "Stephanie Meyer"
                },
                {
          name: "Frankeinstein",     
          img: "/assets/3.5b82b28a.jpg",
          author: "Mary Shelley"
                },
                {
          name: "Harry Potter e a pedra filosofal",     
          img: "/assets/0.2516068b.jpg",
          author: "JK Rowling"
                },
                {
          name: "Harry Potter e a pedra filosofal",     
          img: "/assets/0.2516068b.jpg",
          author: "JK Rowling"
                },
                
                
        
      ],
    };
  },
};
</script>



<style scoped>

.page-title{

  font-family: 'Open Sans';
  font-style: normal;
  font-weight: 600;
  font-size: 60px;
  line-height: 82px;
  max-width: 80%;
  margin-left: 10%; 
  margin-right: 10%;
  margin-top: 187px;
}
.grid-container{
  display: flex;
  justify-content: center;
  align-self: center;
}

.book-grid{
  display: flex;
  flex-wrap: wrap;
  max-width: 80%;
  margin-top: 20px;
  margin-left: 8%; 
  margin-right: 8%;
  margin-bottom: 80px;
}

.book{
  color: black;
  display: flex;
    justify-content: row;
    flex-direction: column;
    width: 19vw;
    height: 50vh;
    margin: 6px;
}

@media screen and (max-width: 1200px) {

.book{
  color: black;
  display: flex;
    justify-content: row;
    flex-direction: column;
    width: 18vw;
    height: 50vh;
    margin: 6px;
}



}

@media screen and (max-width: 600px) {

.book{
  color: black;
  display: flex;
    justify-content: row;
    flex-direction: column;
    width: 60vw;
    height: 50vh;
    margin: 6px;
}


.page-title{

  margin-top: 18px;
}
}



</style>