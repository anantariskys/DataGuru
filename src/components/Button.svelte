<script>
    export let variant = 'primary';
  
    // Define styles based on the variant
    let buttonClass = '';
  
    if (variant === 'primary') {
      buttonClass = 'bg-[#6342FF] text-white hover:bg-opacity-90'; 
    } else {
      buttonClass = 'bg-gray-300 text-black';
    }
  </script>
  
  <button class={`py-2 px-4 text-xl active:scale-95 duration-300 transition-all   ${buttonClass}`}>
    <slot/>
  </button>
  
  
  