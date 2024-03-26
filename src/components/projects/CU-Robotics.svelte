<script>
    import StaticGallery from "./StaticGallery.svelte";
    let robots = [
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
                <span class="text-violet-500"> CU Robotics </span> 
                <div class="py-4"></div>
                
                <p class="poppins text-center text-base sm:text-lg md:text-xl">
                    Currently I am the <span class="text-violet-500"> AutoAim Lead </span>
                    on CU Boulder's RoboMasters team. I have been developing an armor plate detector using
                    <span class="text-violet-500"> OpenCV </span> to find the pixel that is in the center
                    of any armor plates detected in a given frame and then using the depth frame from the
                    <span class="text-violet-500"> Intel RealSense </span> I am able to turn that into a 
                    positon in 3D space relative to our robot.
                </p>
                <div class="py-6"></div>
                <img src="images/cu-robotics/robotics-team.png" alt="">
                <div class="py-4"></div>
                demos comming soon...
                <br />
            </h2>
        </div>
    </section>

<div ><StaticGallery image_src={robots}/></div>
    