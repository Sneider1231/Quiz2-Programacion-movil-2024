<template>
  <ion-page>
    <ion-header>
      <ion-toolbar color="primary">
        <ion-title>Registro de Estudiante</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true" class="ion-padding">
      <ion-grid>
        <ion-row>
          <ion-col size="12" size-md="6" offset-md="3">
            <ion-card>
              <ion-card-content>
                <DatosComunesComponent/>
              </ion-card-content>
            </ion-card>
            <ion-button expand="block" @click="submitForm">Registrarse</ion-button>
            <ion-toast :isOpen="showToast" message="Tu registro se ha completado exitosamente" duration="3000" onIonDidDismiss="showToast = false"></ion-toast>
          </ion-col>
        </ion-row>
      </ion-grid>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonGrid, IonRow, IonCol, IonCard, IonCardContent, IonItem, IonLabel, IonInput, IonSelect, IonSelectOption, IonButton, IonToast } from '@ionic/vue';
import { ref } from 'vue';
import DatosComunesComponent from '@/components/DatosComunesComponent.vue';


const formData = ref({
  firstName: '',
  lastName: '',
  studentID: '',
  major: ''
});

const showToast = ref(false);

const validateName = (event: any) => {
  const inputValue: string = event.target.value;
  // Expresión regular que solo permite letras y espacios
  const regex = /^[a-zA-Z\s]*$/;
  if (!regex.test(inputValue)) {
    // Si el valor no coincide con la expresión regular, eliminamos el último carácter ingresado
    formData.value.firstName = inputValue.slice(0, -1);
  }
};

const validateLastName = (event: any) => {
  const inputValue: string = event.target.value;
  // Expresión regular que solo permite letras y espacios
  const regex = /^[a-zA-Z\s]*$/;
  if (!regex.test(inputValue)) {
    // Si el valor no coincide con la expresión regular, eliminamos el último carácter ingresado
    formData.value.lastName = inputValue.slice(0, -1);
  }
};

const submitForm = () => {
  // Aquí puedes enviar los datos a través de una solicitud HTTP o realizar cualquier otra acción necesaria
  console.log(formData.value);
  // Mostrar la notificación
  showToast.value = true;
};
</script>

<style scoped>
ion-card {
  margin-top: 20px;
}
</style>

