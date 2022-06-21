<template>
  <div id="app">
    <Comentarista name="Matheus" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Comentarista from "./components/Comentarista.vue";

// componentes em TS
@Component({
  components: {
    Comentarista,
  },
})
export default class App extends Vue {}
</script>
