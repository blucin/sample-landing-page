<script>
  export let imageUrl = '';
  export let cardTitle = '';
  export let cardDescription = '';
  import { Card } from 'flowbite-svelte';
</script>

<Card>
  <img src={imageUrl} alt="Card Image" class="h-20 w-20 self-center dark:invert dark:hue-rotate-180"/>
  <h5 class="mb-2 text-2xl text-center font-semibold tracking-tight text-gray-900 dark:text-white">{cardTitle}</h5>
  <p class="mb-3 text-center font-small lg:font-normal text-gray-500 dark:text-gray-400">{cardDescription}</p>
</Card>