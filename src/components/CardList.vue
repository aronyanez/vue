<template>
  <div>
    <h1>lista de cards</h1>
     Prueba: {{valor}}
    <div v-for="contador in 20">
      <span v-if="contador==5">Contador: {{contador}}</span>
      <span v-else-if="contador==1">ELSE IF: {{contador}}</span>
      <span v-else>Otro numero: {{contador}}</span>
    </div>

    <card-twitter v-for="item in 20" :key="item"></card-twitter>
  </div>
</template>

<script>
import CardTwitter from "@/components/CardTwitter.vue";
export default {
  components: {
    CardTwitter
  },

  data() {
    return {
      valor: "prueba"
    };
  },

  beforeCreate() {
    console.log("Before create");
  },
  created() {
    console.log("Iniciar");
    this.valor = 100;
  },
  beforeMount() {
      console.log("antes de mostrar dom");
  },
  mounted() {
     console.log("montado"); 
  },
};
</script>

<style lang="css">
</style>