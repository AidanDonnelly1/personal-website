<script>
    import StaticGallery from "../Generic/Gallery/StaticGallery.svelte";

    let daisy = [
        "images/pets/daisy.jpg",
        "images/pets/daisy-looking.jpg",
        "images/pets/daisy-jakob.jpg",
        "",
        "",
        "",
        "",
        "",
        "",
    ];

    let sylvia = [
        "images/pets/sylvia-kitten.jpg",
        "images/pets/sylvia-basket.jpg",
        "images/pets/sylvia-window.jpg",
        "",
        "",
        "",
        "",
        "",
        "",
    ];

    let bear = [
        "images/pets/bear-not-walking.jpg",
        "images/pets/bear-standing.jpg",
        "images/pets/bear-laying.jpg",
        "",
        "",
        "",
        "",
        "",
        "",
    ];
</script>

<section
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
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Daisy
        </h3>
    </div>

<div class="py-8"></div>

<div id="daisy"><StaticGallery image_src = {daisy} /></div>

<div class="py-8"></div>

<div
        class="flex flex-col gap-4 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Sylvia
        </h3>
    </div>

<div class="py-8"></div>

<div id="sylvia"><StaticGallery image_src = {sylvia} /></div>

<div class="py-8"></div>

<div
        class="flex flex-col gap-4 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            Bear
        </h3>
    </div>

<div class="py-8"></div>

<div id="bear"><StaticGallery image_src = {bear} /></div>
