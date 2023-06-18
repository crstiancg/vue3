<template>
	<h3>{{ contador }}</h3>
	<button :onClick="aumentar">Aumentar</button>
	<button :onClick="disminuir">Disminuir</button>
</template>

<script lang="ts" setup>
import { ref } from "vue";
const contador = ref(0);
// const disabled = ref(0);
const aumentar = () => {
	contador.value++;
	console.log(contador.value);
};
const disminuir = () => {
	if (contador.value > 0) {
		contador.value--;
	}
};
</script>

<style scoped>

h3{
	color: #000;
	font-size: 2em;
}

</style>