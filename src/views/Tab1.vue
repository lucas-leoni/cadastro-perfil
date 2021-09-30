<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Cadastro</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <div class="container">
        <div class="bg">
          <ion-col>
            <div class="avatar">
              <ion-fab-button href="/tabs/tab2">
                <ion-icon :icon="personCircle"></ion-icon>
              </ion-fab-button>
            </div>
            <ion-item class="item">
              <ion-label position="floating">Nome</ion-label>
              <ion-input
                type="text"
                v-model="inputNome"
                required="true"
              ></ion-input>
            </ion-item>
            <ion-item class="item">
              <ion-label>Data de Nascimento</ion-label>
              <ion-input type="date" v-model="inputData"></ion-input>
            </ion-item>
            <ion-item class="item">
              <ion-label position="floating">Telefone</ion-label>
              <ion-input type="number" v-model="inputTel"></ion-input>
            </ion-item>
            <ion-button @click="salvarInformacoes">Salvar</ion-button>
            <h6>
              Nome: {{ nome }} | Data de Nascimento: {{ data }} | Telefone:
              {{ telefone }}
            </h6>
          </ion-col>
        </div>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { personCircle } from "ionicons/icons";
import {
  IonPage,
  IonHeader,
  IonToolbar,
  IonTitle,
  IonContent,
  IonCol,
  IonItem,
  IonLabel,
  IonInput,
  IonFabButton,
  IonButton,
  IonIcon,
} from "@ionic/vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "Tab1",
  components: {
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonPage,
    IonCol,
    IonItem,
    IonLabel,
    IonInput,
    IonFabButton,
    IonButton,
    IonIcon,
  },
  methods: {
    salvarInformacoes() {
      const nome = this.inputNome;
      this.nome = nome;
      const data = this.inputData;
      this.data = data;
      const telefone = this.inputTel;
      this.telefone = telefone;
    },
  },
  data() {
    return {
      inputNome: "",
      nome: "",
      inputData: "",
      data: "",
      inputTel: "",
      telefone: "",
    };
  },
  setup() {
    return {
      personCircle,
    };
  },
});
</script>

<style scoped>
.container {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #dfe6e9;
}
.bg {
  padding: 20px;
  border-radius: 5px;
  background-color: #b2bec3;
}
.item {
  margin: 0px 0px 40px 0px;
}
.avatar {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0px 0px 20px 0px;
}
ion-icon {
  width: 100%;
  height: 100%;
}
</style>
