<script>
export default {
  name: "mIconButton",
  props: {
    cor: String,
    icone: String,
    texto: String,
    func: Function,
    value: String
  }
};
</script>

<template>
  <v-tooltip bottom>
    <template v-slot:activator="{ on }">
      <v-hover v-slot:default="{ hover }">
        <v-btn
          text
          icon
          id="sla"
          v-on="on"
          :color="`${hover ? cor : 'gray'}`"
          v-on:click="func(value)"
        >
          <v-icon> {{ icone }}</v-icon>
        </v-btn>
      </v-hover>
    </template>
    <span> {{ texto }}</span>
  </v-tooltip>
</template>
