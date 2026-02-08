<script>
    export let y;

    let tabs = [
        {name: 'Projects', link: "#projects"},
        {name: 'About Me', link: "#about"}
    ]
</script>

<header class="sticky z-50 top-0 duration-200 px-6 flex items-center justify-between border-b border-solid py-4 bg-slate-950 border-green-800">
    <h1 class="font-medium">
        <b class="font-bold poppins text-green-500">Justin</b> Billeci
    </h1>
    <div class="sm:flex ml-auto pr-4 items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a href={tab.link} class="duration-200 hover:text-green-400">
                <p>{tab.name}</p>
            </a>
        {/each}
    </div>

    <a href="https://www.linkedin.com/in/justinbilleci/" target="_blank" class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950">
        <div class="absolute top-0 right-full w-full h-full bg-green-700 opacity-20 group-hover:translate-x-full z-0 duration-200">
        </div>
        <h4 class="relative z-40">Get in touch</h4>
    </a>

</header>