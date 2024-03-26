
<script>
    /**
     * @type {string[]}
     */
     export let image_src;
</script>
<div class="grid grid-cols-2 md:grid-cols-3 gap-2">
    <div class="grid gap-2">
        <div>
            <img class="h-auto max-w-full rounded-lg" src={image_src[0]} alt="">
        </div>
        <div>
            <img class="h-auto max-w-full rounded-lg" src={image_src[1]} alt="">
        </div>
        <div>
            <img class="h-auto max-w-full rounded-lg" src={image_src[2]} alt="">
        </div>
    </div>
    <div class="grid gap-2">
        <div>
            <img class="h-auto max-w-full rounded-lg" src={image_src[3]} alt="">
        </div>
        <div>
            <img class="h-auto max-w-full rounded-lg" src={image_src[4]} alt="">
        </div>
        <div>
            <img class="h-auto max-w-full rounded-lg" src={image_src[5]} alt="">
        </div>
    </div>
    <div class="grid gap-2">
        <div>
            <img class="h-auto max-w-full rounded-lg" src={image_src[6]} alt="">
        </div>
        <div>
            <img class="h-auto max-w-full rounded-lg" src={image_src[7]} alt="">
        </div>
        <div>
            <img class="h-auto max-w-full rounded-lg" src={image_src[8]} alt="">
        </div>
    </div>
    <!-- <div class="grid gap-4">
        <div>
            <img class="h-auto max-w-full rounded-lg" src={image_src[0]} alt="">
        </div>
        <div>
            <img class="h-auto max-w-full rounded-lg" src="https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-10.jpg" alt="">
        </div>
        <div>
            <img class="h-auto max-w-full rounded-lg" src="https://flowbite.s3.amazonaws.com/docs/gallery/masonry/image-11.jpg" alt="">
        </div>
    </div> -->
</div>
