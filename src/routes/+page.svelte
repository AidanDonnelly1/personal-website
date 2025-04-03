<!-- src/routes/+page.svelte -->
<script>
    import { onMount } from 'svelte';
    import Main from '../components/Main.svelte';
    
    // Sections data
    const sections = [
        { id: 'aboutMe', title: 'About Me' },
        { id: 'education', title: 'Education' },
        { id: 'experience', title: 'Experience' },
        // { id: 'hobbies', title: 'Hobbies' }
    ];
    
    let activeSection = 'about';
    
    // Handle scroll to update active section
    onMount(() => {
        const handleScroll = () => {
            const scrollPosition = window.scrollY + window.innerHeight / 3;
            
            sections.forEach((section) => {
                const element = document.getElementById(section.id);
                if (element) {
                    const offsetTop = element.offsetTop;
                    const offsetHeight = element.offsetHeight;
                    
                    if (scrollPosition >= offsetTop && scrollPosition < offsetTop + offsetHeight) {
                        activeSection = section.id;
                    }
                }
            });
        };
        
        window.addEventListener('scroll', handleScroll);
        return () => window.removeEventListener('scroll', handleScroll);
    });

    let isMobile = false;
  
    onMount(() => {
        const checkMobile = () => {
        isMobile = window.innerWidth < 768; // Tailwind's md breakpoint
        };
        
        checkMobile();
        window.addEventListener('resize', checkMobile);
        
        return () => window.removeEventListener('resize', checkMobile);
  });
    
    // Smooth scroll to section
    const scrollToSection = (id) => {
        activeSection = id;
        const element = document.getElementById(id);
        if (element) {
            element.scrollIntoView({ 
                behavior: 'smooth',
                block: 'center'
            });
        }
    };
</script>

{#if !isMobile}
<div class="flex min-h-screen">
    <!-- Vertical Navbar - Fixed and Centered -->
    <nav class="fixed left-0 top-0 h-screen w-36 flex items-center justify-center pr-0 mr-0">
        <ul class="space-y-6 pl-8 w-full">
            {#each sections as section}
                <li class="w-full h-full">
                    <button
                        class={`text-left py-2 rounded transition-all duration-300 ${activeSection === section.id ? 'text-green-700 font-bold scale-105' : 'text-gray-500 hover:text-green-800'}`}
                        on:click={() => scrollToSection(section.id)}
                    >
                        <span class="relative pl-4">  <!-- Added padding-left here -->
                            {section.title}
                            {#if activeSection === section.id}
                                <span class="absolute left-0 top-1/2 transform -translate-y-1/2 w-1.5 h-3 bg-green-800 rounded-full"></span>
                            {/if}
                        </span>
                    </button>
                </li>
            {/each}
        </ul>
    </nav>

    <!-- Main Content -->
    <main class="ml-36 flex-1 w-full">
        <div class="w-full max-w-4xl mx-auto px-0 py-8">
            <Main />
        </div>
    </main>
</div>
{:else}
<div class="flex min-h-screen">
    <!-- Main Content -->
    <main class="mx-6 flex-1 w-full">
        <div class="w-full max-w-4xl mx-auto px-0 py-8">
            <Main />
        </div>
    </main>
</div>
{/if}