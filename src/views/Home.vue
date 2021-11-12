<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Blank</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Blank</ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-list>
        <ion-item>
          <ion-button expand="block" @click="doit('Naked')">Naked</ion-button>
        </ion-item>
        <ion-item>
          <ion-label>
            <ion-button expand="block" @click="doit('In a Label')"
              >In a Label</ion-button
            >
          </ion-label>
        </ion-item>
        <ion-item>
          <div style="flex: auto">
            <ion-button expand="block" @click="doit('In a div')"
              >In a Div</ion-button
            >
          </div>
        </ion-item>
        <ion-item button @click="doit('button item')"
          ><ion-label>Button Item</ion-label></ion-item
        >
      </ion-list>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import {
  IonButton,
  IonContent,
  IonHeader,
  IonItem,
  IonLabel,
  IonList,
  IonPage,
  IonTitle,
  IonToolbar,
} from "@ionic/vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "Home",
  components: {
    IonButton,
    IonContent,
    IonHeader,
    IonItem,
    IonLabel,
    IonList,
    IonPage,
    IonTitle,
    IonToolbar,
  },
  setup() {
    const doit = (tag: string) => {
      alert(tag);
    };

    return { doit };
  },
});
</script>

<style scoped></style>
