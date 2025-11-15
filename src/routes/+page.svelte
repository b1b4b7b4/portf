<script>
	const portfolio = {
		// "telegram bot",
		// "candles shop",
		// "whisky auction",
		// "whisky parser / aggregator",
		"electric shop": {
			url: "https://infoelectro77.ru/",
		},
		// "oshplay",
		// "clothing shop",
		// "vps service",
		"pinescript strategies / indicators": {
			url: "https://github.com/b1b4b7b4/pinescriptgrind",
		},
		"usn course platform": {
			url: "https://study.usnexpert.com/",
		},
		"riga trip": {
			url: "https://rigatrip.com/",
		},
		"lotos casino": {
			url: "https://lotos-casino.site/",
		},
		"horo.ai": {
			url: "https://myhoro.ai/ru/",
		},
		photostudio: {
			url: "https://dev.sova.photo/",
		},
		// "dabas lase",
		"airway cargo": {
			url: "https://willowy-gnome-e667b3.netlify.app/",
		},
		"solana trader": {
			url: "https://github.com/b1b4b7b4/solana-jup-wrapper",
		},
		// "solo stacking platform",
		// "orbs game",
		// "mobile spins casino ",
		// "garazh managment system",
		// "whisky auctions search"
		"aurorium landing": {
			url: "https://auroiumtest.netlify.app/",
		},
	};
</script>

<div class="grid grid-cols-1 gap-[30px] px-5 mb-5">
	{#each Object.entries(portfolio) as [name, { url }]}
		<button
			onclick={() => (window.location.href = url)}
			class="w-full cursor-pointer flex items-center justify-center bg-black/20 rounded-2xl py-[13px] px-2 min-h-[100px] text-center text-gray-400 text-sm font-medium font-['Poppins'] mb-[5px]"
		>
			{name}
		</button>
	{/each}
</div>
