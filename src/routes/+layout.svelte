<script>
	import './layout.css';
	import "../app.css";
	import favicon from '$lib/assets/favicon.ico';

	import Header from "../components/Header.svelte";
  	import Footer from "../components/Footer.svelte";

	let { children } = $props();

		let y;
		let innerHeight = 0
		let innerWidth = 0

	function goTop() {
		document.body.scrollIntoView()
	}
</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>

<div class="relative flex flex-col max-w-350 mx-auto w-full text-sm sm:text-base min-h-screen">
	
	<div class={"fixed bottom-0 w-full duration-200 flex p-10 z-50" + (
		y > 0 ? 'opacity-100 pointer-events-auto': 'pointer-events-none opacity-0'
	)}>
		<!-- svelte-ignore a11y_consider_explicit_label -->
		<button onclick={goTop} class="ml-auto rounded-full bg-slate-900 text-violet-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer">
			<i class="fa-solid fa-arrow-up grid place-items-center aspect-square"></i>
		</button>
	</div>
	<Header y={y}/>
	{@render children()}
	<Footer/>

</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />