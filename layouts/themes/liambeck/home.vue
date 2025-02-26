<template>
	<div>
		<header>
			<h1 class="text-3xl font-bold underline">
				{{ title }}
			</h1>
		</header>
		<main>
			<div>
				{{ description }}
			</div>
			<div>
				<NuxtLink to="/archives">
					Read all posts
				</NuxtLink>
			</div>
		</main>
	</div>
</template>
<script setup lang="ts">
defineProps<{ doc: unknown; }>()
const config = useAppConfig()
const title = config.name
const description = config.description
</script>
