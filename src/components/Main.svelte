<script>
	import Step from './Step.svelte';

	let steps = [
		{ name: 'SmolJames Store', icon: 'fa-solid fa-cart-shopping' },
		{ name: 'Ultimate To-dos', icon: 'fa-solid fa-list-check' },
		{ name: 'Pokedex', icon: 'fa-solid fa-diagram-project' }
	];

	let benefits = [
		{ name: 'a self taught developer', description: 'Lorem ipsum....' },
		{ name: 'a product design & UX fanatic', description: 'Lorem ipsum....' },
		{ name: 'an excellent communicator', description: 'Lorem ipsum....' }
	];
</script>

<main class="flex flex-col flex-1 p-4">
	<section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
		<div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
			<h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
				Hi! I'm <span class="poppins text-violet-400">Jonathan</span> Bethancourt
				<br /> Senior Software QA <span class="poppins text-violet-400">Engineer</span>
			</h2>
			<p class="text-base sm:text-lg md:text-xl">
				My <span class="text-violet-400">favorite tech</span> includes JS, SvelteKit, Tailwind (other....)!
			</p>
			<a
				href="https://www.linkedin.com/in/jbethancourt/"
				target="_blank"
				class="poppins blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
			>
				<div
					class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
				/>
				<h4 class="relative z-9">Get in touch &rarr;</h4>
			</a>
		</div>
		<div class="relative shadow-2xl grid place-items-center">
			<img src={'images/profile.png'} alt="profile" class="object-cover z-[2] max-h[70vh]" />
		</div>
	</section>

	<section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
		<div class="flex flex-col gap-2 text-center">
			<h6 class="text-lg sm:text-xl md:text-2xl">A few of my creative endeavors.</h6>
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
				Curious to <span class="poppins text-violet-400">see</span> my work?
			</h3>
		</div>
		<a
			href="https://youtube.com"
			target="_blank"
			class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
		>
			<i class="fa-regular fa-circle-play" />
			Watch the video
		</a>

		<div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
			<Step step={steps[0]}>
				<p>
					SmolJames Store is a merchandizing store with <strong class="text-violet-400"
						>Next.js, Commerce.js, Stripe, &amp; Express.js!</strong
					>
				</p>
			</Step>
			<Step step={steps[1]}>
				<p>
					Ultimate Todos is a fullstack todo checklist application <strong class="text-violet-400"
						>Next.js, Commerce.js, Stripe, &amp; Express.js!</strong
					> CRUD application for keeping track of personalized To-Dos w/ login and cross-device persistence
				</p>
			</Step>
			<Step step={steps[2]}>
				<p>
					Pokedex is a <strong class="text-violet-400"
						>Next.js, Commerce.js, Stripe, &amp; Express.js!</strong
					>
				</p>
			</Step>
		</div>
	</section>

	<section
		id="about"
		class="py-20 pt-10 lg:pt16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
	>
		<div
			class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700
        after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
		>
			<h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
			<h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
				A bit <span class="poppins text-violet-400">about</span> me.
			</h3>
		</div>
		<p class="popins mx-auto font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
		<div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
			{#each benefits as benefit, index}
				<div class="flex gap-6 sm:gap-8">
					<p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
						0{index + 1}
					</p>
					<div class="flex flex-col gap-6 sm:gap-8">
						<h3 class="text-2xl sm:text-3xl md:text-5xl">
							{benefit.name}
						</h3>
						<p>
							{benefit.description}
						</p>
					</div>
				</div>
			{/each}
		</div>
		<h5 class="poppins text-2xl sm:text-3xl font-semibold text-center">
			The <span class="poppins text-violet-400">Complete</span> Package(yuck!)
		</h5>
		<div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
			<table class="bg-white text-slate-700 rounded text-center">
				<thead class="border-b border-solid border-slate-200">
					<tr class="">
						<th />
						<th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
						<th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
						<th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
						<th class="whitespace-nowrap p-4 px-8 bg-violet-700 text-white">Me</th>
					</tr>
				</thead>
				<tbody>
					<tr class="border-b border-solid border-slate-200">
						<td
							class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
							>Dedication</td
						>
						<td><i class="fa-solid fa-check text-green-500" /></td>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-check text-green-500" /></td>
					</tr>
					<tr class="border-b border-solid border-slate-200">
						<td
							class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
							>Critical Thinking</td
						>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-check text-green-500" /></td>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-check text-green-500" /></td>
					</tr>
					<tr class="border-b border-solid border-slate-200">
						<td
							class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
							>Interpersonal Skills</td
						>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-check text-green-500" /></td>
						<td><i class="fa-solid fa-check text-green-500" /></td>
					</tr>
					<tr class="border-b border-solid border-slate-200">
						<td
							class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
							>Programming Ability</td
						>
						<td><i class="fa-solid fa-check text-green-500" /></td>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-xmark text-slate-500" /></td>
						<td><i class="fa-solid fa-check text-green-500" /></td>
					</tr>
				</tbody>
			</table>
		</div>
		<div class="mx-auto -mt-12 italic sm:hidden opacity-50">
			<p>Scroll to see more &rarr;</p>
		</div>
		<p class="mx-auto">So why not invest?</p>
	</section>
</main>
