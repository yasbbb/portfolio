<script lang="ts">
	import Dropdown from '$lib/Dropdown.svelte';
	import Project from '$lib/Project.svelte';
	import Nav from '../lib/Nav.svelte';

	const experiences = [
		{
			index: 1,
			name: 'Tech For Good',
			details: 'Software Engineering',
			description: `
				<p>Designed and implemented a kinematics conversion measurement framework into a scalable simulation to
				reduce inconsistency between tailored scenarios impacting 15+ schools across Africa and India. 
				Migrated critical calibration models to OSSFTGG’s open-source software initiative to create enterprise applications
				using OpenTRS saving $35k per year by reducing computation windows</p>
			`,
			technologies: ['PYTHON', 'JAVA', 'GIT']
		},
		{
			index: 2,
			name: 'MDP',
			details: 'Data Product Engineering',
			description: `
				<p>Metadata Engine - Data Discovery	and Extraction</p>
			`,
			technologies: ['PYTHON', 'FLASK', 'TYPESCRIPT', 'DOCKER', 'DATAHUB', 'GKE']
		},
		{
			index: 3,
			name: 'FechAI',
			details: 'Co-Founder',
			description: `
				<a href="https://www.linkedin.com/company/fechai/" target="_blank" style="text-decoration: underline">FECHAI</a>
				<p>Comprehensive platform where we empower users without technical skills to integrate AI-driven applications into their daily lives. Our flagship product Flare is an AI-powered search engine that integrates your favorite tools.</p>
			`,
			technologies: ['SPACY', 'KUBERENETES', 'MONGODB', 'PSQL', 'AWS', 'ELASTICSEARCH']
		},
		{
			index: 4,
			name: 'Stanford',
			details: 'Student Instructor',
			description: `
				<a href="https://codeinplace.stanford.edu/" target="_blank" style="text-decoration: underline">CODE IN PLACE</a>
				<p>Conducted Stanford’s Code in Place CS106A course, engaging 1600+ students globally over 6 weeks. Educated students in Python leveraging beginner-friendly libraries such as Stanford’s Karel and Tinker.</p>
			`,
			technologies: ['PYTHON']
		},
		{
			index: 5,
			name: 'Comerica bank',
			details: 'Cybersecurity',
			description: `
					<p>Crafted queries to facilitate IP-based account flagging algorithms designed to monitor credit card fraud cross-referencing incoming transactions against Comerica Bank’s database. 
					Tightened training model windows, streamlining workflow procedure efficiency by 18% and saving designers ~4500 hours a year
</p>
				`,
			technologies: ['PYTHON', 'CI/CD', 'GIT', 'SHELL', 'LINUX', 'SQL']
		},
		{
			index: 6,
			name: 'Choice Hotels',
			details: 'Software Engineering',
			description: `
				<p>Overhauled serverless deployment process through EC2 instance packaging, 
				creating monthly OS images during Amazon release updates. 
				Migrated 1,800+ jobs to a new AWS Jenkins server using automation scripts and 
				integrated a product design tool API utilized by the operations team to automate design uploads to PostgreSQL 
</p>
			`,
			technologies: ['JAVA', 'AWS', 'JENKINS', 'PACKER', 'PSQL']
		}
	];

	const copyEmailToClipboard = () => {
		navigator?.clipboard?.writeText('yash.bardhan09@gmail.com');
	};
</script>

<svelte:head>
	<title>yash bardhan</title>
	<meta name="description" content="Daniel Kasabov-Nouvion. Developer @ Austin, TX" />
</svelte:head>

<!-- <Nav /> -->

<div class="flex-1 w-full">
	<div class="flex flex-col justify-center pt-10 w-full">
		<p class="text-justify text-white f-code">
			Hey there, I'm Yash Bardhan. I'm a full time Computer Science Student @ UT Dallas. Beyond school, I spend my time as Co-Founder & CEO of FechAI.
			Interested in low level quantitative development. Take a
			look at what I've done and shoot me an
			<span on:click={copyEmailToClipboard} class="cursor-pointer hover:border-b-2"
				>email <svg
					xmlns="http://www.w3.org/2000/svg"
					fill="none"
					viewBox="0 0 24 24"
					stroke-width="1.5"
					stroke="currentColor"
					class="inline-block w-4 h-4"
				>
					<path
						stroke-linecap="round"
						stroke-linejoin="round"
						d="M15.666 3.888A2.25 2.25 0 0013.5 2.25h-3c-1.03 0-1.9.693-2.166 1.638m7.332 0c.055.194.084.4.084.612v0a.75.75 0 01-.75.75H9a.75.75 0 01-.75-.75v0c0-.212.03-.418.084-.612m7.332 0c.646.049 1.288.11 1.927.184 1.1.128 1.907 1.077 1.907 2.185V19.5a2.25 2.25 0 01-2.25 2.25H6.75A2.25 2.25 0 014.5 19.5V6.257c0-1.108.806-2.057 1.907-2.185a48.208 48.208 0 011.927-.184"
					/>
				</svg>
			</span> if you have any questions.<br/><br/>

			shout out <a href="https://www.youtube.com/watch?v=B4C-zUT_Hac" target="__blank" class="underine font-bold text-blue-500">kevin gates</a>
			
		</p>
	</div>
	<div class="py-10">
		<Dropdown options={['EXPERIENCES']} />
	</div>
	<div class="flex flex-col gap-y-10 mb-10 w-full">
		{#each experiences as experience, i}
			<Project {experience} />
		{/each}
	</div>
</div>
