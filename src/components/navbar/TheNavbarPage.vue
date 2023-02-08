<template>
  <div>
    <nav class="navbar navbar-expand navbar-customer fixed-top paddingNav">
        <div class="nav navbar-nav w-100">
          <div class="row w-100">
            <div v-if="!loginstatus" class=" col-9 d-flex">
              <a class="nav-item nav-link active text-white img-survol" href="#" aria-current="page">Pourquoi choisir Le parfait gentmen
              </a>
              <span class="mx-3 text-white pt-2">|</span>
              <a class="nav-item nav-link text-white img-survol" href="#">Nos histoire à succès</a>
            </div>
            <div v-else class=" col-9 d-flex ">
              <TheLoginPage></TheLoginPage>
            </div>

              <div class=" col-3  d-flex justify-content-center align-items-center">
                <a @click="showLogin()" class="deco text-white">LOGIN</a>
                <span class="badge"><i v-if="!loginstatus" class="bi bi-chevron-down fs-5"></i><i v-else class="bi bi-chevron-up fs-5"></i></span>
              </div>
          </div>
        </div>
    </nav>
  </div>
</template>
<script>

import TheLoginPage from '../login/TheLoginPage.vue';

export default {
  components:{TheLoginPage},
  data() {
    return {
      loginstatus:false
    }
  },
  methods: {
    showLogin(){
      this.loginstatus = !this.loginstatus
    }
  },
}
</script>
<style>
  .navbar-customer{
    background-color: rgba(31,37,50,0.9) !important;

  }
  .deco{
    text-decoration: none;
    cursor: pointer;
  }
  .img-survol:hover{
    color:rgb(27, 27, 179)
  }
  .paddingNav{
    padding: 4px !important;
  }
</style>