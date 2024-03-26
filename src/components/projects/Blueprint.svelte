<script>
    import StaticGallery from "./StaticGallery.svelte";
    let blueprint = [
        "",
        "",
        "",
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
            class="px-16 flex flex-col lg:justify-center text-center lg:text-left gap-8 md:gap-10 lg:gap-12"
        >
            <h2
                class="text-center font-semibold text-4xl sm:text-5xl md:text-6xl"
            >
                <span class="text-violet-500"> Blueprint Boulder </span> 
                <div class="py-4"></div>
                <p class="poppins text-center text-base sm:text-lg md:text-xl">
                    Blueprint Boulder is a non-profit and club at CU Boulder that creates
                    websites for other non-profits. Currently I am a <span class="text-violet-500"> Project Lead </span>
                    for the 24-25 year and will update this with more information as it comes
                </p>

                <div class="py-8"></div>
                demos comming soon...
                <br />
            </h2>
        </div>
    </section>

    <StaticGallery image_src={blueprint}/>