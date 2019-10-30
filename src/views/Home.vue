<template>
  <div class="home">
    <v-hover v-slot:default="{ hover }">
      <img
        :src="
          `${
            hover
              ? require('../assets/tetora2.png')
              : require('../assets/tetora1.png')
          }`
        "
      />
    </v-hover>
    <h1>Components go here:</h1>
    <br />
    <h2>Button time!!</h2>
    <v-container>
      <v-row align="center" justify="center">
        <mIconButton
          cor="#DF380F"
          icone="mdi-cancel"
          texto="Cancelar"
          :func="funcao"
          value="Eu cancelo coisas"
        />
        <mIconButton
          cor="#6F53E9"
          icone="mdi-printer"
          texto="Visualizar impressão"
          :func="funcao"
        />
        <mIconButton
          cor="#FFC400"
          icone="mdi-calendar"
          texto="Agendar retorno"
          :func="funcao"
        />
        <mIconButton
          cor="#008C88"
          icone="mdi-arrow-right"
          texto="Transferir"
          :func="funcao"
        />
        <mIconButton
          cor="#6F53E9"
          icone="mdi-plus-circle-outline"
          texto="Novo processo"
          :func="funcao"
        />
        <mIconButton
          cor="#FFC400"
          icone="mdi-content-save"
          texto="Salvar"
          :func="funcao"
        />
        <mIconButton
          cor="#008C88"
          icone="mdi-check-circle"
          texto="Finalizar"
          :func="funcao"
        />
      </v-row>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src
import mIconButton from "@/views/m_icon_button.vue";
export default {
  name: "home",
  components: {
    mIconButton
  },
  methods: {
    funcao(coisa) {
      coisa ? alert(coisa) : alert("Fiz algo");
    }
  }
};
</script>

<style>
img {
  max-width: 350px;
  height: auto;
  margin-left: auto;
  margin-right: auto;
  display: block;
}

h2,
h1 {
  text-align: center;
}
</style>
