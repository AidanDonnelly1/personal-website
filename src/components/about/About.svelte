<script>
    import Gallery from "./Gallery.svelte";
    let image_src = [
        "images/bear.jpg",
        "images/drive-team.jpg",
        "images/new-robot.jpg",
        "images/friends.jpg",
        "images/sylvia.jpg",
        "images/audens-mom.jpg",
        "",
        "",
        "",
    ];
</script>

<div class="py-8"></div>

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

<Gallery {image_src} />
