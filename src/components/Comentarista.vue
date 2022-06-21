<template>
  <div>
    <button @click="comentar()">Comentar</button>
    <p>
      {{ comentario }}
    </p>
    <p>Nome: {{ name }}</p>
  </div>
</template>

// lang = ts
<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
import { Prop } from "vue-property-decorator";
// indica que essa class é um "COMPONENTE"
@Component
export default class Comentarista extends Vue {
  // private da acesso somente dentro
  // public da acesso ao template...etc

  // data em TS
  public comentario = "";
  // prop em TS
  // prop em TS
  @Prop({ required: true, default: "Developer" }) public readonly name!: string;

  // methods em TS
  public comentar(): void {
    this.comentario = "Um mega comentario bem bacana";
  }
  // computed em TS
  get detalhes(): string {
    return `Nome do comentarista: ${this.name}`;
  }
}
</script>

<style></style>
