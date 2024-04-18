<script>
    let display = true;
    function toggleDisplay()
    {
        display = true; 
    }
</script>

<p class="text-center">
    <button
        class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
        on:click={toggleDisplay}
        >
        <div
            class="absolute top-0 right-full w-full h-full bg-violet-500 opacity-20 group-hover:translate-x-full z-0 duration-200"
        />
        <h4 class="relative z-9">Get in touch &rarr;</h4>
        <p>{display}</p>
    </button>
</p>

{#if display}
    <div>test</div>
    <p>asas</p>
    <p>asas</p>
    <p>asas</p>
    <p>asas</p>
    <p>asas</p>
{:else}
   
{/if}
