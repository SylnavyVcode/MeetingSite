<template>
  <div>
    <section class="container-fluid bga vh-120">
      <div class="container p-5">
        <div class="row justify-content-center align-items-center">
          <div class="col-10">
            <div class="row">
              <div class="col-6 first "></div>
              <div class="col-6 p-5 text-white ">
                

                <div class="mb-3">
                  <label for="" class="form-label">First Name</label>
                  <input type="text"
                    class="form-control" name="" id="" aria-describedby="helpId" placeholder="">
                  <small id="helpId" class="form-text text-danger">Help text</small>
                </div>

                <div class="mb-3">
                  <label for="" class="form-label">Last Name</label>
                  <input type="text"
                    class="form-control" name="" id="" aria-describedby="helpId" placeholder="">
                  <small id="helpId" class="form-text text-danger">Help text</small>
                </div>

                <div class="mb-3">
                  <label for="" class="form-label">Email</label>
                  <input type="email" class="form-control" name="" id="" aria-describedby="emailHelpId" placeholder="abc@mail.com">
                  <small id="emailHelpId" class="form-text text-danger">Help text</small>
                </div>

                <div class="mb-3">
                  <label for="" class="form-label">Password</label>
                  <input type="password" class="form-control" name="" id="" placeholder="">
                  <small id="emailHelpId" class="form-text text-danger">Help text</small>
                </div>
               
                <div class="mb-3">
                  <label for="" class="form-label">Confirm Password</label>
                  <input type="password" class="form-control" name="" id="" placeholder="">
                  <small id="emailHelpId" class="form-text text-danger">Help text</small>
                </div>

                <div class="mb-3">

                </div>
                <div class="mb-3 text-center">
                  <button class="btn btn-info"></button>
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
export default {};
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
