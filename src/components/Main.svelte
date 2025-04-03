<script>
    let base = "";
    try {
        // @ts-ignore
        base = process.argv.includes("dev")
            ? ""
            : "https://aidandonnelly1.github.io/personal-website";
    } catch {}

   
    import GraduationTimer from "./EducationSection/GraduationTimer.svelte";
    import Education from "./EducationSection/Education.svelte";
    import ClassProjects from "./EducationSection/ClassProjects.svelte";
    import Modal from "./Modal.svelte";
    import Experience from "./Experience.svelte";
    import IAmTyping from "./IAmTyping.svelte";


    let showModal = false;
</script>

<main class="flex flex-col flex-1">
    <section
        id="aboutMe"
        class="grid grid-cols-1 lg:grid-cols-1 gap-4 pt-8"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-8 md:gap-10 lg:gap-12"
        >
            <h2
                class="text-center font-semibold text-4xl sm:text-5xl md:text-6xl"
            >
                Hi! I'm <span class="poppins text-green-700"
                    >Aidan Donnelly</span
                >
                <br />
            </h2>

            <IAmTyping/>

            <p class="poppins text-center text-base sm:text-lg md:text-xl">
                I am an aspiring Software Engineer studying for a BS in
                <span class="text-green-700"> Computer Science </span>
                at the University of Colorado, Boulder and minoring in
                <span class="text-green-700"> Applied Mathmatics.</span>
                Click on any pictures in the Gallery to see what I've done
            </p>
            <p class="text-center">
                <button
                    on:click={() => (showModal = true)}
                    class="greenShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-stone-900"
                >
                    <div
                        class="absolute top-0 right-full w-full h-full bg-green-900 opacity-20 group-hover:transtone-x-full z-0 duration-200"
                    />
                    <h4 class="relative z-9">Get in touch &rarr;</h4>
                </button>
            </p>
            <Modal bind:showModal/>
        </div>
    </section>

    <section
        id="education"
        class="grid grid-cols-1 lg:grid-cols-1 gap-10 py-8 sm:py-14 mt-0"
    >
        <div
            class="flex flex-col gap-4 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-green-900 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-green-900 py-4"
        >
            <!-- <h6 class="text-large sm:text-xl md:text-2xl">take</h6> -->
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Education
                <!-- <span class="poppins text-green-400">Gallery</span> -->
            </h3>
        </div>
        <div class="w-full justify-content-center">
            <Education/>
            <GraduationTimer/>
            <ClassProjects/>
        </div>
        
    </section>
    <section
        id="experience"
        class="grid grid-cols-1 lg:grid-cols-1 gap-4"
    >
        <div
            class="flex flex-col gap-4 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-green-900 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-green-900 py-4"
        >
            <!-- <h6 class="text-large sm:text-xl md:text-2xl">take</h6> -->
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Experience
                <!-- <span class="poppins text-green-400">Gallery</span> -->
            </h3>
        </div>
        <Experience/>
    </section>
 
</main>

