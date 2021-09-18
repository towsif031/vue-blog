<template>
	<div class="home">
		<h1>Home</h1>
		<p></p>
		<PostList :posts="posts" />
	</div>
</template>

<script>
import PostList from '../components/PostList.vue';
import { ref } from '@vue/reactivity';

export default {
	name: 'Home',
	components: { PostList },
	setup() {
		const posts = ref([
			{
				title: 'welcome to the blog',
				body:
					'Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta explicabo accusamus vel consequatur eaque? Dignissimos necessitatibus unde quasi tempore esse ab voluptatibus molestiae sunt corrupti corporis nihil, nemo laboriosam repudiandae? Soluta expedita deleniti necessitatibus libero perferendis, vero nobis at autem quos, harum accusamus laudantium! Hic quod minus voluptatem possimus quaerat pariatur quis, quo, error rerum commodi est molestiae quae, culpa omnis assumenda facilis quasi reprehenderit consequuntur dicta consequatur! Delectus, aliquam iusto. Excepturi officiis ipsum maiores veritatis rem voluptatum corrupti, reiciendis facere optio, natus quam voluptatibus esse officia eligendi perferendis alias, facilis incidunt animi voluptate amet asperiores! Aut modi doloribus dolores.',
				id: 1
			},
			{ title: 'top 5 CSS tips', body: 'lorem ipsum', id: 2 }
		]);

		return { posts };
	}
};
</script>
