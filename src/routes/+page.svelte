<script lang="ts">
	import Dropdown from '$lib/Dropdown.svelte';
	import Project from '$lib/Project.svelte';
	
	const experiences = [
		{
			index: 999,
			name: 'MLH',
			details: 'Software Engineering',
			description: `
				<a href="https://mlh.io/" target="blank" style="text-decoration: underline">MLH</a>
				<p>Expected to work closely with the Meta Programming Language and Runtime (PL&R) Team to analyze performance between Clang and GCC compilers</p>
			`,
			technologies: ['C++']
		},
		{
			index: 1,
			name: 'TFG',
			details: 'Software Engineering',
			description: `
				<p>Modeled an interactive kinematics simulation with an integrated conversion measurement framework, 
				impacting 15+ schools across Africa and India. 
				Migrated training and calibration models to OSSFTGG’s open-source software initiative</p>
			`,
			technologies: ['PYTHON', 'TYPESCRIPT', 'MATLAB', 'GIT']
		},
		// {
		// 	index: 2,
		// 	name: 'MDP',
		// 	details: 'Data Product Engineering',
		// 	description: `
		// 		<p>Metadata Engine - Data Discovery	and Extraction</p>
		// 	`,
		// 	technologies: ['PYTHON', 'FLASK', 'TYPESCRIPT', 'DOCKER', 'DATAHUB', 'GKE']
		// },
		{
			index: 2,
			name: 'FechAI',
			details: 'Co-Founder',
			description: `
				<a href="https://www.linkedin.com/company/fechai/" target="_blank" style="text-decoration: underline">FECHAI</a>
				<p>Comprehensive platform where we empower users without technical skills to integrate AI-driven applications into their daily lives. Our flagship product Flare is an AI-powered search engine that integrates your favorite tools.</p>
			`,
			technologies: ['SPACY', 'KUBERENETES', 'MONGODB', 'PSQL', 'AWS', 'ELASTICSEARCH']
		},
		{
			index: 3,
			name: 'Stanford',
			details: 'Student Instructor',
			description: `
				<a href="https://codeinplace.stanford.edu/" target="_blank" style="text-decoration: underline">CODE IN PLACE</a>
				<p>Conducted Stanford’s Code in Place CS106A course, engaging 1600+ students globally over 6 weeks. Educated students in Python leveraging beginner-friendly libraries such as Stanford’s Karel and Tinker.</p>
			`,
			technologies: ['PYTHON']
		},
		{
			index: 4,
			name: 'Comerica Bank',
			details: 'Cybersecurity',
			description: `
					<p>Crafted IP-based account flagging algorithms cross-referencing 30k+ transactions against Comerica’s database (CC Fraud). 
					Tightened training model windows using ATF, streamlining workflow procedure efficiency, saving designers ~4500 hours a year
</p>
				`,
			technologies: ['JAVA', 'PYTHON', 'CI/CD', 'GIT', 'SHELL', 'SQL']
		},
		{
			index: 5,
			name: 'Choice Hotels',
			details: 'Software Engineering',
			description: `
				<p>Overhauled EC2 instance deployment process to create OS images during Amazon monthly updates. 
				Migrated 1,800+ jobs to new AWS Jenkins server and integrated a product design tool API to automate design uploads to PostgreSQL 
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
	<meta name="description" content="Yash Bardhan" />
</svelte:head>

<!-- <Nav /> -->

<div class="flex-1 w-full">
	<div class="flex flex-col justify-center pt-10 w-full">
		<p class="text-justify text-white f-code">
			Hey there, I'm Yash Bardhan. I'm a full time CS/Finance Student @ UT Dallas. I'll be working at Major League Hacking as a SWE intern in fall 2024.
			Interested in low level development. Take a
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

			<a href="https://drive.google.com/file/d/1hWwdt3OvTG5hx3UvcSAz01igJf201JDv/view?usp=sharing" target="__blank" class="underine font-bold text-blue-500">my resume</a>
			
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
