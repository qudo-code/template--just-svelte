<script lang="ts">
  import {
    Nav,
  } from "@/components";

  import { Home } from "@/pages";

  const routes = {
    "/": Home,
  };

  $: component = routes[window.location.pathname as keyof typeof routes];
</script>

<Nav />

<main>
  {#if component}
    <svelte:component this={component} />
  {:else}
    <div>
      Loading...
    </div>
  {/if}
</main>
