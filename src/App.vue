<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Paper from './components/Paper.vue';
import Header from './components/Header.vue';
import Additional from './components/Additional.vue';
import Experience from './components/Experience.vue';
</script>

<template>
	<Paper>

		<Header />

		<main class="mt-8 p-4 flow">

			<section>
				<h2 class="underline">Objective</h2>
				<p>Joining a reputable health care organization as a Graduate Nurse to provide exceptional patient care, utilize my quick learning abilities to work hard, implement health care practices, grow and develop my nursing experiences and skills.</p>
			</section>

			<section>
				<hr>
				<span>» </span>
				<h2>Education</h2>
				<div class="flow">
					<div>
						<span class="font-bold">BSN, Bachelor of Science in Nursing, April 2014 </span>
						<span>Central Philippine University, Iloilo City, Philippines</span>
					</div>
					<div>
						<span class="font-bold">Ferndale High School, June 2008 </span>
						<span>Ferndale, Michigan</span>
					</div>
					<div>Current with AHA Health Care Provider BLS</div>
				</div>
			</section>

			<section>
				<hr>
				<span>» </span>
				<h2>Work Experience</h2>

				<div class="flow">
					<Experience />
				</div>

			</section>

			<section>
				<hr>
				<span>» </span>
				<h2 class="highlight">Additional Experiences</h2>
				<div class="flow">
					<Additional />
				</div>
			</section>

		</main>

	</Paper>
</template>

<style>
#app {
	@apply bg-slate-300
		grid place-content-center
		p-4;
}
header span,
h2 {
	@apply text-amber-600;
}
h2 {
	@apply inline-block;
}
</style>
