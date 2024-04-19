<script>
    let base = ""
    try
    {
        base = process.argv.includes('dev') ? "" : "https://aidandonnelly1.github.io/personal-website"
    }
    catch{}
    /**
     * @type {number}
     */
     export let y;

    // export let tabs = [
    //     { name: "About Me", link: base + "/about" },
    //     { name: "Work Experience", link: base + "/work" },
    //     { name: "Projects", link: base + "/projects" },
    //     // { name: "Contact", link: "" },
    // ];
</script>

<header
    class="sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid py-6 bg-transparent border-transparent"
>
    <h1 class="font-medium">
        <a href={base + "/personal-website"} class="hover:text-violet-500 fa-solid fa-house"> </a>
    </h1>
    <!-- <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab}
            <a
                href={tab.link}
                class="duration-200 hover:text-violet-500"
            >
                <p>{tab.name}</p>
            </a>
        {/each}
    </div> -->
</header>