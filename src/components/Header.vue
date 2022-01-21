<script setup lang="ts">
const data = {
	name: "Earl A. Morales",
	contact: [
		"(248) 525-0490",
		"earl.amorales@gmail.com",
		"Pleasant Ridge MI",
	],
}
</script>
<template>
	<header class="flex justify-between items-end">
		<h1>{{ data.name }}</h1>
		<div class="flex flex-col">
			<span v-for="ea in data.contact"
				class="text-right"
			>{{ ea }}</span>
		</div>
	</header>
</template>
<style scoped>
h1 {
	font-size: 4rem;
	line-height: 1;
}
</style>