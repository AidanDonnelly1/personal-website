<script>
    import PetGallery from "./StaticGallery.svelte";

    let daisy = [
        "images/pets/daisy.jpg",
        "images/pets/daisy.jpg",
        "images/pets/daisy.jpg",
        "",
        "",
        "",
        "",
        "",
        "",
    ];

    let sylvia = [
        "images/pets/sylvia.jpg",
        "images/pets/sylvia.jpg",
        "images/pets/sylvia.jpg",
        "",
        "",
        "",
        "",
        "",
        "",
    ];

    let bear = [
        "images/pets/bear.jpg",
        "images/pets/bear.jpg",
        "images/pets/bear.jpg",
        "",
        "",
        "",
        "",
        "",
        "",
    ];
</script>

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
                Meet My <span class="poppins text-violet-500"
                    >Pets</span
                >
                <br />
            </h2>
        </div>
    </section>

<div
        class="flex flex-col gap-4 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
        <!-- <h6 class="text-large sm:text-xl md:text-2xl">take</h6> -->
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Daisy
            <!-- <span class="poppins text-violet-400">Gallery</span> -->
        </h3>
    </div>

<div class="py-8"></div>

<PetGallery image_src = {daisy}/>

<div class="py-8"></div>

<div
        class="flex flex-col gap-4 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
        <!-- <h6 class="text-large sm:text-xl md:text-2xl">take</h6> -->
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Sylvia
            <!-- <span class="poppins text-violet-400">Gallery</span> -->
        </h3>
    </div>

<div class="py-8"></div>

<PetGallery image_src={sylvia}/>

<div class="py-8"></div>

<div
        class="flex flex-col gap-4 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
        <!-- <h6 class="text-large sm:text-xl md:text-2xl">take</h6> -->
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Bear
            <!-- <span class="poppins text-violet-400">Gallery</span> -->
        </h3>
    </div>

<div class="py-8"></div>

<PetGallery image_src={bear}/>
