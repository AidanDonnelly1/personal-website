<script>
    export const prerender = true;
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "CU Robotics",
            icon: "fa-solid fa-robot",
            description:
                "temp",
        },
        {
            name: "Blueprint Boulder",
            icon: "fa-solid fa-hand-holding-heart",
            description:
                "temp",
        },
        {
            name: "Work Experience",
            icon: "fa-solid fa-user",
            description:
                "temp",
        },  
    ];

    let benefits = [
        {
            name: "Computer Science",
            description:
                "Carefully crafting and designing amazing user experiences allows me to express and experiment with every morsel of creativity I have. I love the challenge of learning new design concepts and enabling users with amazing online experiences.",
        },
        {
            name: "CU Robotics",
            description:
                "Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.",
        },
        {
            name: "Blueprint Boulder",
            description:
                "Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Aidan Donnelly</span> 
                <br />
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                Hello <span class="text-violet-400"> Lorem ipsum</span>  dolor sit 
                amet, consectetur adipiscing elit, sed do eiusmod tempor 
                incididunt ut labore et dolore magna aliqua.                 
            </p>
            <button
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Get in touch &rarr;</h4>
            </button>
        </div>
    </section>
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>
       
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>

                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                   
                </p>
            </Step>
        </div>
    </section>
    <!-- <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <div class="z-[-1] bg-violet-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div>>
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                <span class="poppins">About Me</span>
            </h3>
        </div>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl font-semibold text-center">
                            {benefit.name}
                        </h3>
                        <p class="text-center">{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
    </section -->
</main>