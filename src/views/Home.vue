<template>
	<div class="home">
		<h1>Home</h1>
		<p ref="p">{{ name }} is the {{ role }} of Deviluke.</p>
		<button @click="handleClick">Click</button>
	</div>
</template>

<script>
import { ref } from '@vue/reactivity';
export default {
	name: 'Home',
	setup() {
		const p = ref(null);
		console.log(p, p.value);

		let name = 'Lala';
		let role = 'Princess';

		const handleClick = () => {
			console.log(p, p.value);
			p.value.classList.add('test');
			p.value.textContent = 'Hello, Yukki!';
		};

		return { name, role, handleClick, p };
	}
};
</script>
