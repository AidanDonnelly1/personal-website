<script>
    let base = process.argv.includes('dev') ? '' : process.env.BASE_PATH
    export const prerender = true;
    /**
     * @type {number}
     */
     export let y;

    export let tabs = [
        { name: "About Me", link: base + "/about" },
        { name: "Work Experience", link: base + "/work" },
        { name: "Projects", link: base + "/projects" },
        // { name: "Contact", link: "" },
    ];
</script>

<header
    class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid " +
        (y > 0
            ? " py-4 bg-slate-950 border-violet-950"
            : " py-6 bg-transparent border-transparent")}
>
    <h1 class="font-medium">
        <!-- <i class="hover:text-violet-500 fa-solid fa-house"></i> -->
        <a href={base + "/"} class="hover:text-violet-500 fa-solid fa-house"> </a>
    </h1>
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab}
            <a
                href={tab.link}
                class="duration-200 hover:text-violet-500"
            >
                <p>{tab.name}</p>
            </a>
        {/each}
    </div>
</header>