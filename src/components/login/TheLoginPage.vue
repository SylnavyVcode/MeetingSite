<template>
  <div>
    <form @submit.prevent="login()" class="row gy-2 gx-3 align-items-center mx-2">
      <div class="col-auto">
        <input v-model="user.email"
          type="email"
          class="form-control rounded-0"
          id="autoSizingInput"
          placeholder="Email"
        />
      </div>
      <div class="col-auto">
        <input v-model="user.password"
          type="password"
          class="form-control rounded-0"
          id="autoSizingInputGroup"
          placeholder="Mot de passe"
        />
      </div>

      <div class="col-auto">
        <button  type="submit" class="btn btn-success fw-bold rounded-1"><i class="bi bi-shield-lock-fill me-2"></i>LOGIN</button>
      </div>
      <div class="col-2">
        <a class="deco text-white text-decoration-underline " href="">Mot de passe oublié ?</a>
      </div>
    </form>
    <div class="row mx-3 text-danger">{{ message }}</div>
  </div>
</template>
<script>
import dataBase from '../data/user.json'
export default {
  data() {
    return {
      user:{
        email:'',
        password:'',
      },
      error:{
        email:false,
        password:false
      },
      database:dataBase,
      message:'',

    }
  },
  methods: {
    login() {
      console.log('bonjour');
      if (this.user.email.trim() === "") {
       
         this.error.email = true;
         console.log(2);

        // Nous verifions si l'adresse mail est rempli et bien rempli
      } else {
        if (this.user.password.trim() === "" || this.user.password.length<=5) {
          console.log(3);
          this.message="Votre mot de passe doit voir au moins 6 caractères "
          this.error.password = true;
          console.log(4);
        } else {
          this.error.email = false;
          console.log(5);
          this.error.password = false;
          console.log(6);

          // Data-Base
          console.log("sv Response !");

         const response =  this.database.users.find(element => {
            return element.email == this.user.email && element.password == this.user.password
          });
          if(response){
            console.log(response);
            this.database.account = []
            this.database.account.push(response)
            this.$router.push('/home')
            
          }else{
            this.message ="vous n'etes inscrit pas, Inscrivez-vous d'abord et connectez-vous ensuite";
          
          }
         
         
        }
      }
    },
  }
};
</script>
<style>
.deco{
  text-decoration: none;
  ;
}
</style>
