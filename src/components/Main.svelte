<script>
	import Step from "./Step.svelte";

    let steps = [
        {name: 'Never Quit', icon: 'fa-regular fa-dumbbell'},
        {name: 'Personal Website', icon: 'fa-regular fa-desktop'},
        {name: 'To Do List', icon: 'fa-regular fa-list-check'}
    ]

</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl"> 
                Hi! I'm <span class="poppins text-green-500">Justin</span> Billeci <br/>Full Stack
                <span class="poppins text-green-500">Devloper</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="poppins text-green-500">favorite tech</span> includes JavaScript (React, Svelte, or Cold Fusion), TailwindCSS, Node.js and much more!
            </p>
            <a href="https://www.linkedin.com/in/justinbilleci/" target="_blank" class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer">
                <div class="absolute top-0 right-full w-full h-full bg-green-700 opacity-20 group-hover:translate-x-full z-0 duration-200">
                </div>
                <h4 class="relative z-40">Get in touch &rarr;</h4>
            </a>
        </div>

        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/profile.jpeg"} 
                alt="picture of me :)" 
                class="object-cover z-20 max-h-[70vh] rounded-full"/>
        </div>
    </section>

    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my past endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl lg:text-5xl">
                Curious to <span class="poppins text-green-500">see</span> my work?
            </h3>
        </div>

        <a href="" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:mb-0 -mt-10 hover:border-green-700 duration-200" >
            <i class="fa-regular fa-circle-play"></i>
            <p>Watch the video</p>
        </a>

        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>Never Quit is a personal workout generator made with 
                    <strong class="text-green-400">React, Next.js, & TailwindCSS</strong>
                </p>
            </Step>

            <Step step={steps[1]}>
                <p>My personal website that you are on now was made with 
                    <strong class="text-green-400">Svelte, Node.js, and TailwindCSS</strong>
                </p>
            </Step>

            <Step step={steps[2]}>
                <p>This my personal to do list that I made with
                    <strong class="text-green-400">React, Node.js, and TailwindCSS</strong>
                </p>
            </Step>
        </div>

    </section>

    <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-green-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-green-700">
            <h6 class="text-lg sm:text-xl md:text-2xl pt-4">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl pb-4">A bit <span class="poppins text-green-500">about</span> me.</h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
        <div classs="flex flex-col gap-20 w-full mx-auto max-w-[800px]">

        </div>
    </section>
</main>