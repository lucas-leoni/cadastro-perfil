<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Perfil</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <div class="container">
        <div class="bg">
          <div class="avatar">
            <ion-fab-button href="/tabs/tab2">
              <ion-icon :icon="personCircle"></ion-icon>
            </ion-fab-button>
          </div>
          <ion-card>
            <ion-card-header>
              <ion-card-title>Nome: {{ nome }}</ion-card-title>
            </ion-card-header>
          </ion-card>
          <ion-card>
            <ion-card-header>
              <ion-card-title> Data de Nascimento: {{ data }} </ion-card-title>
            </ion-card-header>
          </ion-card>
          <ion-card>
            <ion-card-header>
              <ion-card-title> Telefone: {{ telefone }} </ion-card-title>
            </ion-card-header>
          </ion-card>
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
  IonFabButton,
  IonIcon,
  IonCard,
  IonCardHeader,
  IonCardTitle,
} from "@ionic/vue";

export default {
  name: "Tab3",
  components: {
    IonHeader,
    IonToolbar,
    IonTitle,
    IonContent,
    IonPage,
    IonFabButton,
    IonIcon,
    IonCard,
    IonCardHeader,
    IonCardTitle,
  },
  setup() {
    return {
      personCircle,
    };
  },
};
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
