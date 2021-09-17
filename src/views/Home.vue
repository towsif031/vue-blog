<template>
	<div class="home">
		<p>{{ name }} is the {{ role }} of Deviluke.</p>
		<button @click="handleClick">Click</button>
	</div>
</template>

<script>
export default {
	name: 'Home',
	setup() {
		let name = 'Lala';
		let role = 'Princess';

		const handleClick = () => {
			console.log('button clicked.');
		};

		return { name, role, handleClick };
	}
};
</script>
