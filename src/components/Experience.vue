<script setup lang="ts">
const data = [
	{
		header: [
			'Henry Ford Hospital',
			'Macomb, MI',
			'Nurse Assistant', 
			'December 2014 – present',
		],
		body: [
			'Establish rapport, assist patients with their activities of daily living, meals, and elimination',
			'Perform and obtain patient vital signs, capillary blood glucose, and blood draws',
			'Record and document assessments and procedures into EPIC charting system',
			'Collaborate with RN to assist in procedures and report any abnormal findings',
		]
	},
	{
		header: [
			'Walgreens',
			'Madison Heights, MI',
			'Certified Pharmacy Technician',
			'December 2014 – present',
		],
		body: [
			'Collaborate with Pharmacist receiving, analyzing, and processing prescriptions',
			'Communicate with patients and health care providers in resolving issues',
			'Provides excellent customer service and resolves complaints',
			'Bookkeeping, inventory control, and data entry',
		]
	},
	{
		header: [
			'Ridgedale Senior Service, Inc',
			'Oak Park, MI',
			'Licensed Adult Foster Care Home Caregiver',
			'January 2004 - January 2008',
		],
		body: [
			'Assisted with geriatric and dementia care',
			'Facilitated patient ambulation',
			'Managed leisure and social activities',
		]
	}
]
</script>
<template>
	<div v-for="obj in data">
		<div>
			<span class="font-bold">{{ obj.header[0] }}, </span>
			<span>{{ obj.header[1] }}</span>
		</div>
		<div class="italic">
			<span>{{ obj.header[2] }}, </span>
			<span>{{ obj.header[3] }}</span>
		</div>
		<ul>
			<li v-for="ea in obj.body"
				class="list-disc list-inside ml-4"
			>{{ ea }}</li>
		</ul>
	</div>
</template>