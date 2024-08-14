<script>
    export let title = '';
    export let subtitle = '';
  </script>
  
  <div class="flex flex-col items-center">
    <h5 class="text-[#6D6D6D] text-xl font-semibold">{title}</h5>
    <slot name="value" /> 
    <p class="text-sm text-gray-500">{subtitle}</p>
  </div>
  