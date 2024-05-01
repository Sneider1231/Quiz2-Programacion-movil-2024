<template>

<ion-item>
    <ion-label position="stacked">Primer Nombre</ion-label>
    <ion-input placeholder="  " @input="validateName"></ion-input>
  </ion-item>
  <ion-item>
    <ion-label position="stacked">Segundo Nombre</ion-label>
    <ion-input placeholder=" " @input="validateName"></ion-input>
  </ion-item>
  <ion-item>
    <ion-label position="stacked">Primer Apellido</ion-label>
    <ion-input placeholder=" " @input="validateName"></ion-input>
  </ion-item>
  <ion-item>
    <ion-label position="stacked">Segundo Apellido</ion-label>
    <ion-input placeholder="   " @input="validateName"></ion-input>
  </ion-item>
  <ion-item>
    <ion-label position="stacked">Documento</ion-label>
    <ion-select>
      <ion-select-option value="CEDULA CIUDADANIA">CEDULA CIUDADANIA</ion-select-option>
      <ion-select-option value="Carnet de Extranjería">Carnet de Extranjería</ion-select-option>
      <ion-select-option value="Pasaporte">Pasaporte</ion-select-option>
    </ion-select>
  </ion-item>
  <ion-item>
    <ion-label position="stacked">Número de Documento</ion-label>
    <ion-input placeholder=" " @input="validateName"></ion-input>
  </ion-item>

</template>

<script>
    import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonGrid, IonRow, IonCol, IonCard, IonCardContent, IonItem, IonLabel, IonInput, IonSelect, IonSelectOption, IonButton, IonToast } from '@ionic/vue';

</script>