<template>
  <div>
    <div class="loginBox">

      <img src="./assets/img/logo.svg" alt="logo" class="logoMarca">

      <div class="login" style="display: flex; justify-content: center; border-radius: 20px;">
        <div class="text-white" style="width: 350px;">
          <div class="text-container">
            <h5 class="text-center">Testes dos</h5>
            <h2 class="text-center subtitle">Mestres</h2>
          </div>

          <form action="">
            <label>E-mail de Login <span class="obg">*</span></label>
            <input type="text" name="email" id="email" class="form-control mb-3" placeholder="email@mail.com">

            <label>Senha de Acesso <span class="obg">*</span></label>
            <input type="password" name="senha" id="senha" class="form-control" placeholder="senha">
            <button type="submit" id="btn-submit">Entrar Agora</button>
            <div class="text-center create-account">Não tem conta? <a href="#">Crie agora</a></div>
          </form>
        </div>

      </div>
    </div>
    
    <div id="app">
      <div class="personas">
        <img src="./assets/img/ninja1.png" alt="ninja1" class="img-fluid" style="height: 100%">
      </div>
      <div class="personas">
        <img src="./assets/img/ninja2.png" alt="ninja2" class="img-fluid" style="height: 100%">
      </div>
    </div>

  </div>
</template>

<script>
// import login from './components/login.vue'
import "bootstrap/dist/css/bootstrap.min.css"
export default {
  name: 'App',
  // components: {
  //   login
  // }
}
</script>

<style>
@font-face {
  font-family: "CustomMaster";
  src: url('./assets/fonts/cc-monster-master.woff') format('woff');
}

*, .loginBox{
  margin:0;
  padding: 0;
}
#app{
  background-image: url("./assets/img/bg.png");
  height: 100vh;
  display: flex;
}
.create-account {
  margin-top: 25px;
}
h2 {
  font-size: 3rem;
  line-height: 40px;
}
.personas{
  width: calc(100% / 2);
}
.text-center a {
  text-decoration: none;
}
.personas:nth-child(2) img{
  float: right;
}
form {
  margin-top: 30px;
}
.loginBox{
  width: 100vw;
  height: 100%;
  position:absolute;
  z-index: 9999;
  display: flex;
  align-items: center;
  justify-content: center;
}
h5 {
  margin-bottom: 0rem;
}
label {
    display: inline-block;
    font-size: 0.9rem;
    margin-bottom: 10px;
}
.login{
  border: none;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 450px;
  height: 80%;
  background-image: linear-gradient(58deg, #0220580d 35%, #022058d1);
}
.obg{
  color: rgb(224, 47, 47);
  font-weight: 900;
}
.form-control{
 background: linear-gradient(
96deg
, #1d263829, #5d5d5d29);
    color: white;
    border: none !important;
    padding: 12px;
    border-radius: 12px;
}
.form-control:focus{
  border-color: none !important;
  box-shadow: none !important;
}

:focus-visible {
  outline: none !important;;
}

input:focus-visible {
  outline-offset: none !important;
}

.form-control::placeholder{
  color: #646875;
}

#btn-submit {
  width: 100%;
  padding: 8px 20px;
  margin-top: 20px;
  border: none;
  background: #005FFF;
  border-radius: 12px;
  color: white;
  text-align: left;
  font-size: 1.5rem;
}
@media (max-width: 475px) {
  .login {
    width: 350px;
  }
  .form-control, #btn-submit {
    width: 90%;
  }
}
@media (max-width: 370px) {
  .login {
    width: 335px;
  }
}

@media (max-width: 345px)  {
  .login {
    width: 320px;
  }
}

@media (max-width: 600px){
  #app{
    background-image: url("./assets/img/bg.png");
    height: 100vh !important;
    display: flex;
    /* flex-direction: column; */
  }
  .personas:nth-child(2){
    /* border: 3px solid red; */
    height: 45vh !important;
    bottom: 0 !important;
    right: 0;
    position: absolute;
    width: 60%;
  }

  .personas:nth-child(1) > .img-fluid{
    display: none;
  }
}

.subtitle{
  font-family: "CustomMaster", Arial, Helvetica, sans-serif;
}

.logoMarca{
  width: 50px;
  position: absolute;
  z-index: 9999;
  top: 8%;
  left: 56%;
}
</style>
