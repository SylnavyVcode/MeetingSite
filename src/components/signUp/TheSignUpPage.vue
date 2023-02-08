<template>
  <div>
    <section class="container-fluid bga vh-120">
      <div class="container p-3">
        <div class="row justify-content-center align-items-center">
          <div class="col-10">
            <div class="row">
              <div class="col-6 first "></div>
              <div class="col-6 p-2 px-4 text-white ">
                <div class="mb-3">
                  <label  for="" class="form-label">First Name</label>
                  <input v-model="user.firstname" type="text"
                    class="form-control" name="" id="" aria-describedby="helpId" placeholder="">
                  <small id="helpId" class="form-text text-danger">Help text</small>
                </div>

                <div class="mb-3">
                  <label for="" class="form-label">Last Name</label>
                  <input v-model="user.lastname" type="text"
                    class="form-control" name="" id="" aria-describedby="helpId" placeholder="">
                  <small id="helpId" class="form-text text-danger">Help text</small>
                </div>

                <div class="mb-3">
                  <label for="" class="form-label">Email</label>
                  <input v-model="user.email" type="email" class="form-control" name="" id="" aria-describedby="emailHelpId" placeholder="abc@mail.com">
                  <small id="emailHelpId" class="form-text text-danger">{{message.email}}</small>
                </div>

                <div class="mb-3">
                  <label for="" class="form-label">Password</label>
                  <input v-model="user.password" type="password" class="form-control" name="" id="" placeholder="">
                  <small id="emailHelpId" class="form-text text-danger">{{message.password}}</small>
                </div>
               
                <div class="mb-3">
                  <label for="" class="form-label">Confirm Password</label>
                  <input v-model="user.confPassword" type="password" class="form-control" name="" id="" placeholder="">
                  <small id="emailHelpId" class="form-text text-danger">{{message.confPassword}}</small>
                </div>

                <div class="mb-3">

                </div>
                <div class="mb-3 text-center">
                  <button @click="signUp()" type="submit" class="btn btn-info fw-bold text-white">Créer un Compte</button>
                </div>
                
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  data() {
    return {
      user: {
        firstname:'',
        lastname:'',
        email: "",
        password: "",
        confPassword: "",
      },
      message: {
        firstname:"Vous n'avez pas mis le nom",
        lastname:"Vous n'avez pas mis le prénom",
        email: "",
        password: "",
        confPassword: "",
      },
      error: {
        firstname:false,
        lastname:false,
        email: false,
        password: false,
        confPassword: false
      },
      state: true,
    }
  },
  methods: {
    signup(){
      console.log('mange');
      },
    signUp() {
      if (this.user.email.trim() === "") {
        this.error.email = true;
        this.error.password = false;
        this.error.confPassword = false;
        this.message.email = "Vous n'avez pas mis l'adresse email"
      } else {
        if (this.user.password.trim() === "") {
          this.error.password = true;
          this.error.email = false;
          this.error.confPassword = false;
          this.message.password="Vous n'avez pas mis le mot de passe"
        } else {
          if (this.user.confPassword.trim() === "") {
            this.error.confPassword = true;
            this.error.email = false;
            this.error.password = false;
            this.message.confPassword="Vous n'avez pas confirmer le mot de passe"
            }else{
                this.error.email = false;
                this.error.password = false;
                this.error.confPassword = false;
                
                if(this.user.confPassword != this.user.password){
                  this.error.confPassword = true
                  this.message.confPassword ="votre confirmation n'est pas identique au mot de passe"
        
                }else{
                  this.error.confPassword = false
                }

              }  
        }
      }
    },
  }
}
</script>
<style>
.first {
  background-image: url("../../assets/images/rencontre.jpg");
  object-fit: cover;
  border-radius: 10px;
  border: 2px solid rgb(177, 218, 252);
}
.bga{
  background-image: linear-gradient(to right, rgb(224, 143, 143), rgb(12, 136, 105), rgb(181, 14, 247));
}
</style>
