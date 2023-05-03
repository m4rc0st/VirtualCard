<template>
  <div  class="container">
    <h2 class="title"><b>VIRTUAL CARD</b></h2>
    <p >Meu Perfil</p>
  </div>
  <div class="q-pa-md q-gutter-sm">
    <p class="title-infor">Nome Completo</p>
    <q-input
      color="grey-3"
      outlined
      v-model="nome"
      label="Nome Completo"
      maxlength="30"
      >
      <template v-slot:prepend>
        <q-icon class="material-symbols-outlined" name="person" color="grey" />
      </template>
    </q-input>

    <p class="title-infor">Cargo Atual</p>
    <q-input
      color="grey-3"
      outlined
      v-model="cargo"
      label="Cargo Atual"
      maxlength="30"
      >
      <template v-slot:prepend>
        <q-icon class="material-symbols-outlined" name="work" color="grey" />
      </template>
    </q-input>

    <p class="title-infor">Instituição</p>
    <q-input
      color="grey-3"
      outlined
      v-model="instituição"
      label="Instituição de Ensino"
      maxlength="30"
      >
      <template v-slot:prepend>
        <q-icon class="material-symbols-outlined" name="school" color="grey" />
      </template>
    </q-input>
    <br>
    <p>Contatos</p>
    <p class="title-infor">Email</p>
    <q-input
      color="grey-3"
      outlined
      v-model="email"
      label="Email"
      maxlength="30"
      >
      <template v-slot:prepend>
        <q-icon class="material-symbols-outlined" name="mail" color="grey" />
      </template>
    </q-input>

    <p class="title-infor">WhatsApp</p>
    <q-input
      color="grey-3"
      outlined
      v-model="whatsapp"
      label="Whatsapp"
      maxlength="12"
      >
      <template v-slot:prepend>
        <q-icon class="material-symbols-outlined" name="contacts" color="grey" />
      </template>
    </q-input>

    <p class="title-infor">LinkedIn</p>
    <q-input
      color="grey-3"
      outlined
      v-model="linkedin"
      label="LinkedIn"
      >
      <template v-slot:prepend>
        <q-icon class="material-symbols-outlined" name="badge" color="grey" />
      </template>
    </q-input>

    <p class="title-infor">Instagram</p>
    <q-input
      color="grey-3"
      outlined
      v-model="instagram"
      label="Instagram"
      >
      <template v-slot:prepend>
        <q-icon class="material-symbols-outlined" name="auto_stories" color="grey" />
      </template>
    </q-input>
    <br>
    <q-btn
      no-caps
      unelevated
      class="botao"
      label="Salvar informações"
      @click="salvar"
    />
  </div>

</template>

<script>
import { ref } from 'vue'

export default {
  name: 'MyPerfil',
  data(){

  }
}

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
  margin-top: 10px;
}
.title-infor {
  color: rgb(86, 86, 86);
  font-size: 14px;
  padding: 0px 0px 0px 0px;
  margin-top: 10px;
  margin-bottom: 0;
  border-radius: 7px;
}
</style>
