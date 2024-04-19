<script>
    let base = "";
    try {
        base = process.argv.includes("dev")
            ? ""
            : "https://aidandonnelly1.github.io/personal-website";
    } catch {}

    import LinkedGallery from "./Generic/Gallery/LinkedGallery.svelte";

    import Modal from "./Modal.svelte";

    let showModal = false;
    let image_src = [
        "images/pets/bear.jpg", // 0
        "images/drive-team.jpg", // 1
        "images/cu-robotics/new-robot.jpg", // 2
        "images/friends.jpg", // 3
        "images/pets/sylvia.jpg", // 4
        "images/blueprint/intro-meeting.png", // 5
        "",
        "",
        "",
    ];

    let image_link = [
        base + "/pets#bear", // 0
        base + "/projects", // 1
        base + "/projects#cu-robotics", // 2
        base + "/work", // 3
        base + "/pets#sylvia", // 4
        base + "/projects#blueprint", // 5
        base + "",
        base + "",
        base + "",
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-1 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-8 md:gap-10 lg:gap-12"
        >
            <h2
                class="text-center font-semibold text-4xl sm:text-5xl md:text-6xl"
            >
                Hi! I'm <span class="poppins text-violet-500"
                    >Aidan Donnelly</span
                >
                <br />
            </h2>
            <p class="poppins text-center text-base sm:text-lg md:text-xl">
                I am an aspiring Software Engineer studying for a BS in
                <span class="text-violet-500"> Computer Science </span>
                at the University of Colorado, Boulder and minoring in
                <span class="text-violet-500"> Applied Mathmatics.</span>
                Click on any pictures in the Gallery to see what I've done
            </p>
            <p class="text-center">
                <button
                    on:click={() => (showModal = true)}
                    class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
                >
                    <div
                        class="absolute top-0 right-full w-full h-full bg-violet-500 opacity-20 group-hover:translate-x-full z-0 duration-200"
                    />
                    <h4 class="relative z-9">Get in touch &rarr;</h4>
                </button>
            </p>
            <Modal bind:showModal/>
        </div>
    </section>

    <div
        class="flex flex-col gap-4 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
        <!-- <h6 class="text-large sm:text-xl md:text-2xl">take</h6> -->
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Gallery
            <!-- <span class="poppins text-violet-400">Gallery</span> -->
        </h3>
    </div>

    <div class="py-8"></div>

    <LinkedGallery {image_src} {image_link} />
</main>
