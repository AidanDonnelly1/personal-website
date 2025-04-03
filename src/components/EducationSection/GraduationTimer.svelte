<!-- src/routes/GraduationCountdown.svelte -->
<script>
// @ts-nocheck

    import { onMount } from 'svelte';
  
    let years = 0;
    let days = 0;
    let hours = 0;
    let minutes = 0;
    let seconds = 0;
    let hasGraduated = false;
    
    // Set your exact graduation date and time (May 1, 2027 at noon as example)
    const graduationDate = new Date(2027, 4, 1, 12, 0, 0); // Note: months are 0-indexed (4 = May)
  
    onMount(() => {
      const updateCountdown = () => {
        const now = new Date();
        let distance = graduationDate - now;
  
        if (distance <= 0) {
          hasGraduated = true;
          years = days = hours = minutes = seconds = 0;
          return;
        }
  
        // Calculate years
        let yearDiff = graduationDate.getFullYear() - now.getFullYear();
        let tempDate = new Date(now);
        tempDate.setFullYear(now.getFullYear() + yearDiff);
        
        if (tempDate > graduationDate) {
          yearDiff--;
          tempDate.setFullYear(now.getFullYear() + yearDiff);
        }
        
        years = yearDiff;
  
        // Calculate remaining days
        const daysInYear = (/** @type {number | Date} */ date) => {
          const start = new Date(date.getFullYear(), 0, 0);
          const diff = date - start;
          return Math.floor(diff / (1000 * 60 * 60 * 24));
        };
  
        days = daysInYear(graduationDate) - daysInYear(tempDate);
        
        // If days is negative, adjust years and days
        if (days < 0) {
          years--;
          tempDate.setFullYear(tempDate.getFullYear() - 1);
          days = daysInYear(graduationDate) - daysInYear(tempDate);
        }
  
        // Calculate hours, minutes, seconds
        hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        seconds = Math.floor((distance % (1000 * 60)) / 1000);
      };
  
      updateCountdown();
      const interval = setInterval(updateCountdown, 1000);
      return () => clearInterval(interval);
    });
  </script>
  
  <div class="flex flex-col items-center justify-center bg-base-100 p-4">

    <h1 class="text-3xl font-bold mb-4 text-primary">
        {hasGraduated ? 'Congratulations Graduate!' : 'Countdown to College Graduation'}
    </h1>
    
    {#if !hasGraduated}
      <div class="grid auto-cols-max grid-flow-col gap-3 md:gap-5 text-center">
        <!-- Years -->
        <div class="bg-neutral rounded-box text-neutral-content flex flex-col p-3 md:p-4">
          <span class="countdown font-mono text-4xl md:text-5xl">
            <span style={`--value:${years};`}>{years}</span>
          </span>
          years
        </div>
        
        <!-- Days -->
        <div class="bg-neutral rounded-box text-neutral-content flex flex-col p-3 md:p-4">
          <span class="countdown font-mono text-4xl md:text-5xl">
            <span style={`--value:${days};`}>{days}</span>
          </span>
          days
        </div>
        
        <!-- Hours -->
        <div class="bg-neutral rounded-box text-neutral-content flex flex-col p-3 md:p-4">
          <span class="countdown font-mono text-4xl md:text-5xl">
            <span style={`--value:${hours};`}>{hours}</span>
          </span>
          hours
        </div>
        
        <!-- Minutes -->
        <div class="bg-neutral rounded-box text-neutral-content flex flex-col p-3 md:p-4">
          <span class="countdown font-mono text-4xl md:text-5xl">
            <span style={`--value:${minutes};`}>{minutes}</span>
          </span>
          min
        </div>
        
        <!-- Seconds -->
        <div class="bg-neutral rounded-box text-neutral-content flex flex-col p-3 md:p-4">
          <span class="countdown font-mono text-4xl md:text-5xl">
            <span style={`--value:${seconds};`}>{seconds}</span>
          </span>
          sec
        </div>
      </div>
    {:else}
      <div class="text-center p-8 bg-success/20 rounded-lg max-w-md">
        <p class="text-2xl text-success mb-4">🎉 You did it! 🎉</p>
        <p class="text-lg">Congratulations on your graduation!</p>
      </div>
    {/if}
  </div>