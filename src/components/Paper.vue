<script setup lang="ts"></script>

<template>
	<div class="paper">
		<slot></slot>
	</div>
</template>

<style>
.paper {
	@apply bg-white
		w-[8.5in] h-[11in]
		p-[.7in];
}
</style>
