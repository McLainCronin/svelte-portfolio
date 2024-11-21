<script>
	import '../app.css';
    import Footer from '../components/Footer.svelte';
    import Header from '../components/Header.svelte';

	let y;
	let innerHeight;
	let innerWidth;

	function goTop() {
		document.body.scrollIntoView();
	}
</script>


<div class="relative flex flex-col max-w-[1400px] lg:max-w-none mx-auto w-full text-sm sm:text-base min-h-screen">
	<div class={"fixed bottom-0 w-full duration-200 flex p-10 z-[10] " + (y > 0 ? ' opacity-100 pointer-events-auto' : ' pointer-events-none opacity-0')}>
		<button on:click={goTop} class="p-3 ml-auto rounded-full bg-slate-900 text-blue-400 px-3.5 hover:bg-slate-800 cursor-pointer">
			<i class="fa-solid fa-arrow-up grid place-items-center aspect-square"></i>
		</button>
	</div>
	<Header y={y}/>
	<slot />
	<Footer y={y}/>
</div>


<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth/>
