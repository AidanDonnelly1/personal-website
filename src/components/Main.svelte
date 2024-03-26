<script>
    export const prerender = true;
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "CU Robotics",
            icon: "fa-solid fa-robot",
            description:
                "Smoljames Store is a a merchanising store created with Next.js, Commerce.js & Stripe! Commerce.js is a CMS for managing project and Stripe is used for all transaction handling.",
        },
        {
            name: "Blueprint Boulder",
            icon: "fa-solid fa-hand-holding-heart",
            description:
                "Test for model robustness with customized test profiles and receive exhaustive reporting on the performance and potential vulnerabilities of your model.",
        },
        {
            name: "Work Experience",
            icon: "fa-solid fa-user",
            description:
                "Augment your datasets with our filters and dataset manipulations to ensure your models are trained on the highest quality datasets (coming soon).",
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
        class="grid grid-cols-1 lg:grid-cols-1 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="text-center font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-500">Aidan Donnelly</span> 
                <br />
            </h2>
            <p class="text-center text-base sm:text-lg md:text-xl ">
                Hello <span class="text-violet-500"> Lorem ipsum</span>  dolor sit 
                amet, consectetur adipiscing elit, sed do eiusmod tempor 
                incididunt ut labore et dolore magna aliqua.                 
            </p>
            <p class="text-center">
                <button
                    class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
                >
                    <div
                        class="absolute top-0 right-full w-full h-full bg-violet-500 opacity-20 group-hover:translate-x-full z-0 duration-200"
                    />
                    <h4 class="relative z-9">Get in touch &rarr;</h4>
                </button>
            </p>
        </div>
    </section>
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">       
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                   safas asfasf asf as fsa fas fa sfs a s fas fasfafsf a sfaff as sa sf a sfaff as ss fas fasfafsf a sfaff as sa sf a sfaff as s 
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    as fas as fsa fas fas fasfafsf a sfaff as sa sf a sfaff as s fas fasfafsf a sfaff as sa sf a sfaff as ssa sf a sfaff as sa 
            </Step>
            <Step step={steps[2]}>
                <p>
                    fasasf sa fa sfas fasf a sfaff as sa fa sfas fasf a sfaff as sf a sfaff as sa sf a sfaff as sa 
                </p>
            </Step>
        </div>
    </section>
</main>