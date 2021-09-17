<template>
	<div class="home">
		<h1>Home</h1>
		<input type="text" v-model="search" />
		<p>searching for : [ {{ search }} ]</p>
		<div v-for="name in matchingNames" :key="name">{{ name }}</div>
	</div>
</template>

<script>
import { computed, ref } from '@vue/reactivity';
export default {
	name: 'Home',
	setup() {
		const search = ref('');
		const names = ref([
			'Lala',
			'Kotegawa',
			'Yami',
			'Mai',
			'Yui',
			'Asuna',
			'Megumin'
		]);

		const matchingNames = computed(() => {
			return names.value.filter((name) => name.includes(search.value));
		});

		return { names, search, matchingNames };
	}
};
</script>
