<template>
        <main id="modal-promocao" class="modal-r">
            <div class="modal-container">
                <div class="lines">
                    <h3 class="subtitle-form">Login</h3>
                    <form>
                        <input type="text" class="input" placeholder="E-mail:"  v-model="usuario">
                        <br>
                        <br>
                        <input type="password" name="password" class="input" placeholder="Senha:" v-model="senha" >
                        <br>
                        <br>
                <div class="q-gutter-md q-pb-md" v-if="token">
                <q-btn color="primary" label="Logout" @click="efetuarLogout()" />
              </div> 
             </form>
                </div>
                <div class="holes hole-top "></div>
                <div class="holes hole-middle "></div>
                <div class="holes hole-bottom "></div>
                <div class="q-gutter-md q-pb-md botao">
                <q-btn flat rounded color="red-8" style="font-weight: bold;" type="a" href="/" label="Voltar" />
                <q-btn outline rounded style="font-weight: bold;" color="green" label="Login" @click="efetuarLogin()" />
                </div> 
            </div>
        </main>
</template>
<script>
import { mapGetters, mapActions } from 'vuex'

export default {
  name: 'Login',
  data () {
    return {
      usuario: '',
      senha: ''
    }
  },
  methods: {
    ...mapActions('mainstore', ['login','logout','carregarToken']),    
    async efetuarLogin () {
      await this.login({ username: this.usuario, password: this.senha })
      await this.carregarToken()
      if (this.token) {
        this.$router.push('/dashboard')
      }
    },
    efetuarLogout () {
      this.logout()
    }
  },
  computed: {
    ...mapGetters('mainstore', ['token'])
  }
}
</script>
<style scoped>
.modal-container {
    position: center;
    /* width: 100vw;
    height: 100vh; */
   
    z-index: 2000;
    /* display: none; */
    justify-content: center;
    align-items: center;
}
.modal-r:before {
    content: '';
    position: absolute;
    left: 45px;
    top: -2px;
    height: 100%;
    background: #eb3b5a;
}

.modal-container.mostrar {
    display: center;
}
@media screen and (max-width: 400px) {
  .modal-r{
    width: 50%;
  }
}
.botao{
    display: flex;
    justify-content: space-around;
}

.modal-r {
    background: white;
    width: 30%;
    height: 300px;
    min-width: 400px;
    padding: 40px;
    border: 10px solid #a8d8ea;
    border-radius: 5%;
    box-shadow: 0 0 0 10px white;
    position: relative;
    margin: auto;
    margin-top: 200px;
}

.lines {
    margin-top: 40px;
    height: 100%;
    width: 100%;
    background-image: repeating-linear-gradient(white 0px, white 24px, steelblue 25px);
}

.subtitle-form {
    /* position: absolute; */
    font-size: 2rem;
    text-transform: uppercase;
    text-align: center;
    color: #eb3b5a;
    top: 65px;
    left: 55px;
    font-weight: bold;
    bottom: 10px;
    right: 10px;
    line-height: 25px;
    font-family: 'Indie Flower';
    overflow: hidden;
    outline: none;
}

.holes {
    position: absolute;
    left: 10px;
    height: 25px;
    width: 25px;
    background: lightgoldenrodyellow;
    border-radius: 50%;
    box-shadow: inset 0px 0px 2px 0px #888;
}

.hole-top {
    top: 10%;
}

.hole-middle {
    top: 45%;
}

.hole-bottom {
    bottom: 10%;
}

.input,
.button,
.input-select {
    font-family: 'Comfortaa', cursive;
    font-size: large;
    margin-left: 15px;
    border: 0 none;
    width: 90%;
    background-color: transparent;
}

.button {
    cursor: pointer;
}

.button:hover {
    color: #8854d0;
}

.check {
    margin-left: 15px;
    margin-top: 10px;
    font-family: 'Comfortaa', cursive;
}

.input {
    color: black;
    line-height: 20px;
}

.button {
    color: darkgreen;
    font-weight: bold;
    width: 90%;
}

.input-select {
    color: rgb(112, 112, 112);
}

.label {
    color: rgb(112, 112, 112);
    font-size: large;
    font-family: 'Comfortaa', cursive;
}

.input:focus {
    box-shadow: 0 0 0 0;
    border: 0 none;
    outline: 0;
}



</style>