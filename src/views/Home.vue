<template>
	<div class="home">
		<h1>Home</h1>
		<p ref="p">{{ name }} is the {{ role }} of Deviluke.</p>
		<button @click="handleClick">Click</button>
		<button @click="role = 'New Princess'">Make Her Princess</button>
		<input type="text" v-model="name" />
	</div>
</template>

<script>
import { ref } from '@vue/reactivity';
export default {
	name: 'Home',
	setup() {
		const p = ref(null);
		console.log(p, p.value);

		const name = ref('Lala');
		const role = ref('Princess');

		const handleClick = () => {
			name.value = 'Momo';
			role.value = 'daughter of the King';
		};

		return { name, role, handleClick, p };
	}
};
</script>
