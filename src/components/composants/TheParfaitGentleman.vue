<template>
  <div>
    <div class="row row-parfait-gentleman bg-white ombre">
      <div class="col">
        <img class="tailleImg bg-dark" src="@/assets/images/logo1.svg" alt="">
        <h3 class="fst-italic mt-4">Inscription</h3>
        <p class="fst-italic">Des célibataires cultivés dans votre région</p>
        <hr />
        <div class="row">
          <div class="col">
            <p class="fw-bold">Je suis</p>
            <div class="form-check mb-2">
              <input
                class="form-check-input rounded-3 fs-5 "
                type="checkbox"
                value=""
                id="flexCheckChecked1"
               
              />
              <label class="form-check-label" for="flexCheckChecked">
                une femme
              </label>
            </div>
            <div class="form-check">
              <input
                class="form-check-input rounded-3 fs-5 "
                type="checkbox"
                value=""
                id="flexCheckChecked2"
                
              />
              <label class="form-check-label" for="flexCheckChecked">
                une homme
              </label>
            </div>
          </div>
          <div class="col">
            <p class="fw-bold">Je recherche</p>
            <div class="form-check mb-2">
              <input
                class="form-check-input rounded-3 fs-5 "
                type="checkbox"
                value=""
                id="flexCheckChecked3"
                
              />
              <label class="form-check-label" for="flexCheckChecked">
                un homme
              </label>
            </div>
            <div class="form-check">
              <input
                class="form-check-input rounded-3 fs-5 "
                type="checkbox"
                value=""
                id="flexCheckChecked4"
                
              />
              <label class="form-check-label" for="flexCheckChecked">
                une femme
              </label>
            </div>
          </div>
        </div>
        <div class="row">
          <div class="col d-flex justify-content-center">
            <button class="btn btn-hover btn-info mt-3 px-5 py-3 text-white rounded-0 shadow">
              <span class="p-0 m-0 fw-bold fs-5">INSCRIPTION GRATUITE</span>
              </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style>

p, label{
  font-size: 18px;
}
.row-parfait-gentleman{
  position: absolute;
  width: 400 px;
  padding: 20px 25px;
  margin: 0;
  top: 21vh;
  left:5vw;
  overflow: visible;
  z-index: 999;
  background-color: azure;
  
}
.tailleImg{
  width: 340px;
  height: 60px;
}
.ombre{
  box-shadow: -1px 0px 10px rgb(219, 213, 213);;
}
.btn-hover:hover{
  background: rgb(10, 138, 177);
}

</style>
