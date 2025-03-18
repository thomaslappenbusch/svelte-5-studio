<script lang="ts">
	import { Anvil, Aperture, ChevronsUp, House, Phone, WindArrowDownIcon } from 'lucide-svelte';
	import { page } from '$app/state';
	import '../app.css';
	import { goto } from '$app/navigation';
	let { children } = $props();
</script>

<style>
	.specialBG {
		position: relative;
		background-color: #F6F6F6;
	}

	.specialBG::before {
		content: "";
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400' viewBox='0 0 800 800'%3E%3Cg fill='none' stroke='%23CDCDCD' stroke-width='1.2'%3E%3Cpath d='M769 229L1037 260.9M927 880L731 737 520 660 309 538 40 599 295 764 126.5 879.5 40 599-197 493 102 382-31 229 126.5 79.5-69-63'/%3E%3Cpath d='M-31 229L237 261 390 382 603 493 308.5 537.5 101.5 381.5M370 905L295 764'/%3E%3Cpath d='M520 660L578 842 731 737 840 599 603 493 520 660 295 764 309 538 390 382 539 269 769 229 577.5 41.5 370 105 295 -36 126.5 79.5 237 261 102 382 40 599 -69 737 127 880'/%3E%3Cpath d='M520-140L578.5 42.5 731-63M603 493L539 269 237 261 370 105M902 382L539 269M390 382L102 382'/%3E%3Cpath d='M-222 42L126.5 79.5 370 105 539 269 577.5 41.5 927 80 769 229 902 382 603 493 731 737M295-36L577.5 41.5M578 842L295 764M40-201L127 80M102 382L-261 269'/%3E%3C/g%3E%3Cg fill='%23E4E4E4'%3E%3Ccircle cx='769' cy='229' r='7'/%3E%3Ccircle cx='539' cy='269' r='7'/%3E%3Ccircle cx='603' cy='493' r='7'/%3E%3Ccircle cx='731' cy='737' r='7'/%3E%3Ccircle cx='520' cy='660' r='7'/%3E%3Ccircle cx='309' cy='538' r='7'/%3E%3Ccircle cx='295' cy='764' r='7'/%3E%3Ccircle cx='40' cy='599' r='7'/%3E%3Ccircle cx='102' cy='382' r='7'/%3E%3Ccircle cx='127' cy='80' r='7'/%3E%3Ccircle cx='370' cy='105' r='7'/%3E%3Ccircle cx='578' cy='42' r='7'/%3E%3Ccircle cx='237' cy='261' r='7'/%3E%3Ccircle cx='390' cy='382' r='7'/%3E%3C/g%3E%3C/svg%3E");
		mask-image: radial-gradient(circle at top, transparent 30%, rgba(0, 0, 0, 0.5) 90%, rgba(0, 0, 0, 1) 100%);
		-webkit-mask-image: radial-gradient(circle at top, transparent 30%, rgba(0, 0, 0, 0.5) 90%, rgba(0, 0, 0, 1) 100%);
		pointer-events: none;
	}
</style>

<div class="min-h-screen specialBG flex flex-col justify-start items-center">
	<div class="flex justify-between w-full max-w-[1600px] h-20 px-8 z-20 sticky top-0 bg-[#F6F6F6]">
		<div class="flex items-center text-2xl font-medium tracking-tighter">
			<ChevronsUp class="mr-1.5 h-7 w- mb-[1px]" strokeWidth={1.7}/>
			Agios Studio
		</div>
		<div class="flex space-x-10">
			<button 
				onclick={() => goto('/')} 
				class={`cursor-pointer transition-colors duration-200 hover:text-zinc-900 ${page.route.id === '/' ? ' text-black  font-medium' : ' text-zinc-700 '}`}
			>
			Home
			</button>
			<button 
				onclick={() => goto('/portfolio')}
				class={`cursor-pointer transition-colors duration-200 hover:text-zinc-900 ${page.route.id === '/portfolio' ? 'text-black font-medium' : ' text-zinc-700 '}`}
			>
			Portfolio
			</button>
			<button 
				onclick={() => goto('/blog')}
				class={`cursor-pointer transition-colors duration-200 hover:text-zinc-900 ${page.route.id === '/blog' ? 'text-black font-medium' : ' text-zinc-700 '}`}
			>
			Blog
			</button>
			<button class="flex items-center space-x-2 text-[16px] font-medium tracking-tight bg-white my-auto px-4 py-2 border border-zinc-300 rounded-full cursor-pointer"><div>Book a free call</div> <Phone class="h-4 w-4" fill={"#000000"} strokeWidth={.4}/></button>
		</div>
	</div>
	{@render children()}
</div>
