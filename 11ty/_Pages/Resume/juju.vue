<script setup>
const juju = {
	name: "Julia Williams",
	contact: {
		address: "3404 N Central Park Ave.<br>Chicago, IL 60618",
		gmaps: "https://goo.gl/maps/W47LHURMSLPZB3D76",
		phone: "(248) 915-5817",
		email: "williamsjulia21@gmail.com",
		web: "juliawilliams.info",
	},
	experience: [
		{
			header: ["LATITUDE", "Chicago, IL", "Lab Assistant", "JAN 2021- Present"],
			content:
				"Assist lab users with: editing and file management in Photoshop, scanning on Epson V850, Kodak Creo flatbed, and Scanmate drum scanners, Canon, Epson and Piezography small and large format printing, print handling, trimming and packaging. Manage daily tasks and service bureau orders optimizing Trello, Quickbooks, and G Suite.",
		},
		{
			header: ["The California Clipper", "Chicago, IL", "Shift Manager, Bartender", "OCT 2018 - MAR 2020"],
			content:
				"High-volume, high-speed cocktail bartending in a landmark venue setting, personalized guest relations while managing a 2-6 person team, balanced registers and safe, paid-out staff and performing musicians.",
		},
		{
			header: [
				"Cranbrook Art Museum",
				"Bloomfield Hills, MI",
				"Museum Educator, Classroom Coordinator",
				"NOV 2017 - JULY 2018",
			],
			content:
				"Created art lessons based on museum's collections for art camps for ages 5-13, assisted family-centered programs and events based on current exhibitions, delivered grant-funded lessons to the Detroit and Pontiac public schools for grades 3-8, and managed departmental art supplies.",
		},
		{
			header: ["City of Berkley", "Berkley, MI", "Craft Director, Treasury Clerk", "MAY 2014 - JUNE 2016"],
			content:
				"Created art lessons for ~130 children across three summer camps ages 4-13, managed departmental supplies and Google calendar, high-volume POS transactions for individual citizens and other municipal entities, operated BS&A software, performed general office administration, and acted as an election poll worker.",
		},
		{
			header: ["Rosewood Art Centre", "Kettering, OH", "Exhibition Coordinator Intern", "AUG 2013- DEC 2013"],
			content:
				"Assisted exhibition coordinator at the Rosewood Gallery, installed exhibitions, cataloged artists’ solo-exhibitions submission in gallery’s database, assisted with interactive, community-based art demonstrations.",
		},
	],
	education: [
		{
			header: ["University of Dayton", "Dayton, OH", "Bachelor of Arts, Art History", "AUG 2010 - MAY 2014"],
			content: "Cum Laude",
		},
	],
	skills: [
		"Customer Service",
		"Teaching Artist",
		"Youth Development",
		"Succinct Writer",
		"Adaptable",
		"Collaborative",
		"Quick",
		"Passionate",
		"Communicative",
	],
	technical_capabilities: [
		"Mac",
		"PC",
		"C41 & E6 photo chemical processes",
		"Epson, Primefilm, Kodak and Scanmate scanners",
		"BS&A Software",
		"Breadcrumb",
		"Cloudinary",
		"Lightroom",
		"Photoshop",
		"GIMP",
		"G Suite",
		"Microsoft Office",
		"Trello",
	],
}
</script>

<template>
	<article class="resume">
		<section class="name">
			<h1>{{ juju.name }}</h1>
		</section>

		<section class="experience">
			<h2 class="color1">experience</h2>
			<div class="small" v-for="ea in juju.experience">
				<header>
					<h3>{{ ea.header[0] }},</h3>
					<span>{{ ea.header[1] }} — </span>
					<span
						><em>{{ ea.header[2] }}</em></span
					>
				</header>
				<div>
					<span class="lighter smallest">{{ ea.header[3] }}</span>
				</div>
				<p class="lighter small">{{ ea.content }}</p>
			</div>
		</section>

		<section class="education">
			<h2 class="color2">education</h2>
			<div v-for="ea in juju.education">
				<header>
					<h3>{{ ea.header[0] }},</h3>
					<span>{{ ea.header[1] }} — </span>
					<span
						><em>{{ ea.header[2] }}</em></span
					>
				</header>
				<div>
					<span class="lighter smallest">{{ ea.header[3] }}</span>
				</div>
				<p class="lighter smaller">{{ ea.content }}</p>
			</div>
		</section>

		<section class="contact smallest">
			<a v-html="juju.contact.address" href="{{juju.contact.gmaps}}"></a>
			<a href="tel:{{juju.contact.phone}}">{{ juju.contact.phone }}</a>
			<a href="mailto:{{juju.contact.email}}">{{ juju.contact.email }}</a>
			<a href="{{juju.contact.web}}">{{ juju.contact.web }}</a>
		</section>

		<section class="skills">
			<h2 class="color3">skills</h2>
			<ul class="smaller lighter">
				<li v-for="ea in juju.skills">{{ ea }}</li>
			</ul>
		</section>

		<section class="technical-capabilities">
			<h2 class="color4">technical capabilities</h2>
			<ul class="smaller lighter">
				<li v-for="ea in juju.technical_capabilities">{{ ea }}</li>
			</ul>
		</section>
	</article>
</template>

<style>
body {
	background: silver;
}
h1, h2, h3, p, ul {
	margin: 0;
	padding: 0;
}
h1 {
	font-size: 3rem;
}
h2 {
	text-transform: uppercase;
	font-size: 0.75rem;
}
h3 {
	display: inline-block;
	font-size: 16px;
}
header {
	line-height: 1.25;
	font-size: 16px;
}
p {
	line-height: 1.25;
}
header, p, li {
	font-family: serif;
}

.resume {
	line-height: 1.25;
	background: white;
	margin: 0 auto;
	/*
	letter-spacing: -0.025em;
		*/
	/* paper dimensions */
	width: 8.5in;
	height: 11in;
	padding: 0.7in;
	/* 
	border: 1px solid black;
 */
	display: grid;
	gap: 2rem 3rem;
	grid-template-columns: 3fr 1fr;
	grid-template-rows: 0.75fr 2.5fr 4fr 0.75fr;
	grid-template-areas:
		"name contact"
		"experience skills"
		"experience technical-capabilities"
		"education technical-capabilities";
}
.name {
	grid-area: name;
	align-self: center;
}
.experience {
	grid-area: experience;
}
.education {
	grid-area: education;
}
.contact {
	grid-area: contact;
}
.skills {
	grid-area: skills;
}
.technical-capabilities {
	grid-area: technical-capabilities;
}

.resume section > div {
	margin: 1.125rem 0;
}
.resume header + div {
	margin: 0.25rem 0 0.5rem;
	letter-spacing: -0.025em;
	line-height: 0.75rem;
}
.contact a {
	display: block;
	color: black;
}
.contact a:not(:last-child) {
	line-height: 0.75rem;
	margin: 0.375rem 0;
}
.skills li,
.technical-capabilities li {
	display: block;
	margin: 0.75rem 0;
}
.experience h2 {
	color: forestgreen;
}
.education h2 {
	color: steelblue;
}
.skills h2 {
	color: darkgoldenrod;
}
.technical-capabilities h2 {
	color: peru;
}

.small {
	font-size: 14px;
}
.smaller {
	font-size: 12px;
}
.smallest {
	font-size: 10px;
}
.lighter {
	color: dimgray;
}
</style>
