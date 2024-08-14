<script>
    import { onMount } from 'svelte';
  
    let count = 0;
    let target = 0;
    let isVisible = false;
    export let afterNumeric = '+'
  
    export let end = 0;
    export let duration = 2000; 
  
    onMount(() => {
      const observer = new IntersectionObserver(entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            startAnimation();
            observer.unobserve(entry.target); 
          }
        });
      });
  
      observer.observe(document.querySelector('.ticker'));
    });
  
    function startAnimation() {
      target = end;
      const startTime = performance.now();
      const endTime = startTime + duration;
  
      function animate(timestamp) {
        const progress = Math.min((timestamp - startTime) / duration, 1);
        count = Math.floor(progress * target);
        if (progress < 1) {
          requestAnimationFrame(animate);
        }
      }
  
      requestAnimationFrame(animate);
    }
  </script>
  
  <div class="ticker text-3xl font-semibold">{count}{afterNumeric}</div>
  
