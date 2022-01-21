<script setup lang="ts">
const data = {
	content: [
		[
			"Birmingham Dance Academy", 
			"Birmingham, MI",
			"Dance teacher", 
			"October 2014 – present",
		],
		[
			"Annie Divinagracia Sartorio School of Performing Arts",
			"Iloilo City, Philippines",
			"Dance teacher", 
			"June 2008 – June 2013",
		]
	]
}
</script>
<template>
	<div v-for="ea in data.content">
		<div>
			<span class="font-bold">{{ ea[0] }}, </span>
			<span>{{ ea[1] }}</span>
		</div>
		<div class="italic">
			<span>{{ ea[2] }}, </span>
			<span>{{ ea[3] }}</span>
		</div>
	</div>
</template>