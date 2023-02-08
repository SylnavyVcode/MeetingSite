<template>
  <div>
   
    <TheNavbarPage></TheNavbarPage>
    <TheParfaitGentleman @inscrit="inscrit()"></TheParfaitGentleman>
    
    <!-- ========== Start slider bar ========== -->
    
    <div id="carouselId" class="carousel slide" data-bs-ride="carousel">

      <div class="carousel-indicators m-0">
       <infos></infos> 
      </div>
      

      <!-- ========== Start slide body ========== -->
      <div class="carousel-inner" role="listbox">
          <div class="carousel-item active">
            <img src="@/assets/images/image1.jpg" class="w-100 d-block img-carousel" alt="First slide">
          </div>
          <div class="carousel-item">
            <img src="@/assets/images/image2.jpg" class="w-100 d-block img-carousel" alt="Second slide">
          </div>
          <div class="carousel-item">
            <img src="@/assets/images/image3.jpg" class="w-100 d-block img-carousel" alt="Third slide">
          </div>
            <!-- <infos></infos> -->
        </div>
      <!-- ========== End slide body ========== -->
      <!-- ========== End slider bar ========== -->
    </div>


    <!-- ========== Start Bonne Rencontre ========== -->
    <BonneRencontre></BonneRencontre>
    <!-- ========== End Bonne Rencontre ========== -->
    


    <!-- ========== Start Footer ========== -->
    <TheFooterPage></TheFooterPage>
    <!-- ========== End Footer ========== -->


  </div>
</template>

<script>
import TheNavbarPage from '../navbar/TheNavbarPage.vue';
import TheParfaitGentleman from '../composants/TheParfaitGentleman.vue';
import infos from '../composants/infos.vue';
import BonneRencontre from '../composants/BonneRencontre.vue';
import TheFooterPage from '../footer/TheFooterPage.vue';

export default {
  components:{TheNavbarPage, TheParfaitGentleman, infos, BonneRencontre, TheFooterPage},
  methods: {
    inscrit(){
      this.$router.push('/signup')
    }
  },
}
</script>
<style scoped>
*{
  font-family: 'Open Sans', sans-serif;
}

  .img-carousel{
    height: 135vh !important;
    object-fit: cover;
  }

  
  </style>