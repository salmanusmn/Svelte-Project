<script>
  let number = 0

  function add5(){
    number += 5;
  }
  
  $: multiple = number*2 
</script>

<main class="flex flex-col justify-center items-center h-screen space-y-4">
  <p> The number is: {number}</p>
  <button on:click="{add5}" class="btn btn-primary">Add five</button>
  <p>The number multiplied by 2 is {multiple}</p>

  {#if multiple < 50}
  <div class="alert alert-success shadow-lg">
    <div>
      <svg xmlns="http://www.w3.org/2000/svg" class="stroke-current flex-shrink-0 h-6 w-6" fill="none" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>
      <span>Numbers look good!</span>
    </div>
  </div>

  {:else}
  <div class="alert alert-error shadow-lg">
    <div>
      <svg xmlns="http://www.w3.org/2000/svg" class="stroke-current flex-shrink-0 h-6 w-6" fill="none" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>
      <span>Numbers are too high!</span>
    </div>
  </div>
  {/if}
</main>

<style>
</style>