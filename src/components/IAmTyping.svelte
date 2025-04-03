<!-- TypingRoles.svelte -->
<script>
    export let roles = [
        "Software Engineer",
        "Life Long Learner",
        "Innovator", 
        "Problem Solver",
        "Tech Enthusiast"
    ];
    
    export let typingSpeed = 75;
    export let deletingSpeed = 50;
    export let pauseBetweenRoles = 1000;
    
    let roleIndex = 0;
    let charIndex = 0;
    let isDeleting = false;
    let currentText = '';
    
    function typeRoles(node) {
        function tick() {
            if (isDeleting) {
                currentText = roles[roleIndex].substring(0, charIndex - 1);
                charIndex--;
            } else {
                currentText = roles[roleIndex].substring(0, charIndex + 1);
                charIndex++;
            }
            
            node.textContent = currentText;
            
            if (!isDeleting && currentText === roles[roleIndex]) {
                setTimeout(() => {
                    isDeleting = true;
                    tick();
                }, pauseBetweenRoles);
            } else if (isDeleting && currentText === '') {
                isDeleting = false;
                roleIndex = (roleIndex + 1) % roles.length;
                setTimeout(tick, typingSpeed);
            } else {
                setTimeout(tick, isDeleting ? deletingSpeed : typingSpeed);
            }
        }
        
        tick();
    }
</script>
<div class="w-full flex flex-row justify-center poppins text-4xl">
    <h2>
    I am a
        <span class="typing-text text-green-700" use:typeRoles>
            {roles[0]} <!-- Fallback content -->
        </span>
    </h2>
    
</div>


<style>
    .typing-text {
        display: inline-block;
        border-right: 2px solid;
        animation: blink 0.7s infinite;
    }
    
    @keyframes blink {
        0%, 100% { border-color: transparent; }
        50% { border-color: currentColor; }
    }
</style>