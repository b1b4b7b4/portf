<script lang="ts">
	import { goto } from "$app/navigation";
	import { page } from "$app/state";
	import "../app.css";
	import favicon from "$lib/assets/favicon.svg";

	let { children } = $props();
</script>

<svelte:head>
	<link
		rel="icon"
		href={"https://i.pinimg.com/736x/00/17/41/0017417cdb2476a3fb0380e2c8d0a347.jpg"}
	/>
	<title>le buba | portfolio</title>
</svelte:head>

<div class="container max-w-[756px] m-auto my-20">
	<div class=" mb-[50px] flex flex-col items-center">
		<img
			alt="bibabuba"
			class="w-28 h-28 rounded-full mb-10 object-cover"
			src="/me.png"
		/>
		<div
			class="w-96 text-center justify-start text-gray-100 text-3xl font-medium font-['Poppins']"
		>
			Daniil Fedorov
		</div>
		<div
			class="w-96 text-center justify-start text-gray-400 text-sm font-medium font-['Poppins']"
		>
			Full Stack Developer
		</div>
	</div>

	{#snippet textBlock(t: string, v: string)}
		<div class="flex flex-col items-center">
			<div
				class="justify-start text-neutral-300 text-base font-medium font-['Poppins']"
			>
				{t}
			</div>
			<div
				class="w-24 text-center justify-start text-gray-400 text-sm font-medium font-['Poppins']"
			>
				{v}
			</div>
		</div>
	{/snippet}
	<div class="flex justify-around px-5 mb-[68px]">
		{@render textBlock("7", "Years of work experience")}
		{@render textBlock("158", "Completed projects")}
		{@render textBlock("171", "Personal side projects")}
	</div>

	<div class="flex gap-3.5 px-[22px]">
		<button
			onclick={() => goto("/cv.pdf")}
			class="cursor-pointer w-full py-[13px] px-[29px] justify-start text-neutral-700 text-xs font-medium font-['Poppins'] bg-amber-200 rounded-[10px]"
			>Download CV
		</button>
		<button
			onclick={() => (window.location.href = "https://t.me/b1b4b7b4")}
			class="cursor-pointer w-full py-[13px] px-[29px] text-gray-400 text-xs font-medium font-['Poppins'] bg-[#171F26] rounded-[10px] border-blue-800"
			>Contact me
		</button>
	</div>

	{#snippet Togglebtn(txt: string, url: string)}
		<button
			onclick={() => goto(url)}
			class="cursor-pointer w-full text-center justify-start text-gray-400 text-sm font-medium font-['Poppins'] h-12 rounded-[10px] border-blue-800 {page
				.url.pathname == url
				? 'bg-[#0C151D]'
				: 'bg-[#171F26]'}"
			>{txt}
		</button>
	{/snippet}

	<div class="px-[22.5px] py-2.5 mb-[30px] mt-[58px]">
		<div
			class="py-[6px] px-[6px] flex gap-[9px] bg-[#171F26] rounded-[10px]"
		>
			{@render Togglebtn("Portfolio", "/")}
			{@render Togglebtn("Skills", "/skills")}
		</div>
	</div>

	{@render children()}

	<div
		class="text-center justify-start text-gray-400 text-sm font-medium font-['Poppins'] pt-[30px] pb-10"
	>
		@bibabuba
	</div>
</div>
