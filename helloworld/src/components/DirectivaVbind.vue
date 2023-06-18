<template>
    <div>
        <h1 v-bind:class="{
            'error': alert
        }">El mensaje es valido</h1>

        <button :onClick="active">{{ msg }}</button>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const alert = ref(false);
const msg = ref("Activar");


const desactivar = () =>{
    if(msg.value == "Activar"){
        return msg.value = "Deactivar";
    }else{
        return msg.value = "Activar";
    }
}

const active = () =>{
    desactivar();
    if(alert.value == false){
        return alert.value = true;
    }else{
        return alert.value = false;
    }
}

</script>

<style scoped>
.error {
    color: red;
}
</style>