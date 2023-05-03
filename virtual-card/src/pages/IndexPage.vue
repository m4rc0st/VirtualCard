<template>
    <br>
    <div class="container">
      <h2 class="subtitle">
        Bem-vindo!
      </h2>
      <h1 class="title"><b>VIRTUAL CARD</b></h1>
      <h2 class="subtitle">
        Faça login e comece a usar!
      </h2>
    </div>
    <div class="q-pa-md">
      <div class="q-pa-md q-gutter-sm">
      <p class="title-infor">Endereço de Email</p>
      <q-input color="grey-3" outlined  v-model="email" label="Email">
          <template v-slot:prepend>
            <q-icon class="material-symbols-outlined" name="mail" color="grey" />
          </template>
        </q-input>
        <p class="title-infor" >Senha</p>
          <q-input  color="grey-3" outlined v-model="senha" label="Senha">
          <template v-slot:prepend>
            <q-icon class="material-symbols-outlined" name="lock"  color="grey"  />
          </template>
        </q-input>
      </div>
    </div>
    <q-btn
      no-caps
      unelevated
      class="botao"
      label="Entrar na Plataforma"
      @click="logar"
    />
    <br>
    <q-link class="links" tag="a" href="www.exemplo.com.br">Esqueci minha senha</q-link>
    <q-link class="links" tag="a" href="">Não possui conta? Crie uma agora!</q-link>
</template>

<script>
import { ref } from 'vue'

export default ({
  name: 'IndexPage',
  data () {
    return {
      email:"",
      senha:"",
    }
  },
  mounted(){

  },
  methods:{
    async logar(){
      this.$router.push({ name: "perfil" });
    }
  }
})
</script>

<style>

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.title{
  color: #003368;
  font-size: 36px;
  line-height: 1.5;
  margin: 0;
}
.subtitle{
  color: #003368;
  font-size: 16px;
  line-height: 1.5;
  margin: 0;
  margin-top: 5px;
  margin-bottom: 5px;
}
.links{
  font-size: 12px;
  display: flex;
  flex-direction: column;
  align-items: center;
  color: #7C7C8A;
}
.botao{
  font-size: 16px;
  display: flex;
  justify-content: space-between;
  gap: 5px;
  margin-top: 8px;
  margin: 0 auto;
  color: white;
  background-color: #E2A411;
  position: center;
}
.title-infor {
  color: rgb(86, 86, 86);
  font-size: 14px;
  padding: 8px 0px 9px 0px;
  border-radius: 7px;
}
</style>
