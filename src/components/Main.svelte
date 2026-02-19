<script>
	import Step from "./Step.svelte";

    let steps = [
        {name: 'Never Quit', 
        icon: 'fa-regular fa-dumbbell',
        href: "https://neverquit.netlify.app/"},

        {name: 'Personal Website', 
        icon: 'fa-regular fa-desktop',
        href: "https://justinbilleci.netlify.app/"},

        {name: 'askMe', 
        icon: 'fa-regular fa-list-check',
        href: 'https://askmeeee.netlify.app/'},
    ];

    let benefits = [
    {name: 'A self taught developer', 
    description: "I learned to code using free online resources and absolutely fell in love with the process, there's nothing I'd rather do."},
    {name: 'A web design master', 
    description: "I have a strong foundation and excellent work experience with Responsive Web Design, I view this as the strongest part of my skillset."},
    {name: 'A great communicator', 
    description: "Communication is just as important as coding ability in my eyes, so I make an effort to communicate as effectively and clearly as possible."},
    ]

</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
        <div class="flex flex-col lg:justify-center text-center lg:text-left ">
            <!-- Heading Text Start -->
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl pb-10 md:pb-12 lg:pb-14"> 
                Hi! I'm <span class="poppins text-green-500">Justin Billeci</span> <br/>Full Stack
                <span class="poppins text-green-500">Developer</span>
            </h2>
            <!-- Heading text End -->

            <!-- Details Start -->
            <p class="text-base sm:text-lg md:text-xl pb-4 md:pb-6">
                My <span class="poppins text-green-500">Top Skills</span> include <span class="font-semibold poppins">Project Overview</span>, <span class="font-semibold poppins">Project Management</span>, <span class="font-semibold poppins">Team Management</span>, <span class="font-semibold poppins">Client Relations</span>, and <span class="font-semibold poppins">Database Management</span>.
            </p>

            <p class="text-base sm:text-lg md:text-xl pb-4 md:pb-6">
                My <span class="poppins text-green-500">Top Programming Skills</span> include JavaScript (<span class="font-semibold poppins">React</span>, <span class="font-semibold poppins">Svelte</span>, and <span class="font-semibold poppins">Express.js</span>), <span class="font-semibold poppins">TailwindCSS</span>, and <span class="font-semibold poppins">PostgreSQL</span>.
            </p>
            <!-- Details End -->

            <!-- Get In Touch Button Start -->
            <a href="https://www.linkedin.com/in/justinbilleci/" target="_blank" class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer">
                <div class="absolute top-0 right-full w-full h-full bg-green-700 opacity-20 group-hover:translate-x-full z-0 duration-200">
                </div>
                <h4 class="relative z-40">Get in touch &rarr;</h4>
            </a>
            <!-- Get In Touch Button End -->
        </div>

        <!-- Cover Image Start -->
        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/profile.jpeg"} 
                alt="Justin Billeci Cover Pic" 
                class="object-cover z-20 max-h-[70vh] rounded-full"/>
        </div>
        <!-- Cover Image End -->
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

        <!--- <a href="" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:mb-0 -mt-10 hover:border-green-700 duration-200" >
            <i class="fa-regular fa-circle-play"></i>
            <p>Watch the video</p>
        </a> --->

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
                <p>askMe is an ai prompt app made with
                    <strong class="text-green-400">React, Node.js, Express.js, and TailwindCSS</strong>
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
        <div class="flex flex-col gap-20 w-full mx-auto max-w-200">
            {#each benefits as benefits, index}
                <div class="flex gap-6 sm:gap-8">
                    <p class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold">
                        0{index+1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefits.name}
                        </h3>
                        <p>{benefits.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section>
</main>