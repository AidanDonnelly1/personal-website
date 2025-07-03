<script>
  import { onMount } from 'svelte';

  let years = 0, days = 0, hours = 0, minutes = 0, seconds = 0;
  let hasGraduated = false;

  const graduationDate = new Date(2027, 4, 1, 12, 0, 0);   // 1 May 2027 12:00

  onMount(() => {
    const updateCountdown = () => {
      const now       = new Date();
      // @ts-ignore
      const distance  = graduationDate - now;

      if (distance <= 0) {
        hasGraduated = true;
        years = days = hours = minutes = seconds = 0;
        return;
      }

      //-- time constants
      const second = 1000;
      const minute = 60 * second;
      const hour   = 60 * minute;
      const day    = 24 * hour;

      //-- basic units
      const totalDays = Math.floor(distance / day);
      years   = Math.floor(totalDays / 365);      // rough but good enough
      days    = totalDays % 365;

      hours   = Math.floor((distance % day) / hour);
      minutes = Math.floor((distance % hour) / minute);
      seconds = Math.floor((distance % minute) / second);
    };

    updateCountdown();
    const id = setInterval(updateCountdown, 1000);
    return () => clearInterval(id);
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