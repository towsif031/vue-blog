<template>
	<div class="home">
		<p>{{ name }} is the {{ role }} of Deviluke.</p>
	</div>
</template>

<script>
export default {
	name: 'Home',
	setup() {
		let name = 'Lala';
		let role = 'Princess';

		return { name, role };
	}
};
</script>
