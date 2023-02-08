<template>
  <div>
    <form class="row gy-2 gx-3 align-items-center mx-2">
      <div class="col-auto">
        <input
          type="email"
          class="form-control rounded-0"
          id="autoSizingInput"
          placeholder="Email"
        />
      </div>
      <div class="col-auto">
        <input
          type="password"
          class="form-control rounded-0"
          id="autoSizingInputGroup"
          placeholder="Mot de passe"
        />
      </div>

      <div class="col-auto">
        <button type="submit" class="btn btn-success fw-bold rounded-1"><i class="bi bi-shield-lock-fill me-2"></i>LOGIN</button>
      </div>
      <div class="col-2">
        <a class="deco text-white text-decoration-underline " href="">Mot de passe oublié ?</a>
      </div>
    </form>
  </div>
</template>
<script>
export default {};
</script>
<style>
.deco{
  text-decoration: none;
  ;
}
</style>
