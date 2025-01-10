<script lang="ts">
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
  import { Skeleton, ImagePlaceholder, TextPlaceholder } from 'flowbite-svelte';
  import "../app.css";
  let { children } = $props();

  let profiles = [
    ["GitHub", "/ghb.svg", "https://github.com/lemon-gith"],
    ["Idk", "/ghb.svg", "https://github.com/lemon-gith"],
    ["Idk", "/ghb.svg", "https://github.com/lemon-gith"],
  ];
</script>

<div class="relative px-8">
  <Navbar fluid={true} class="fixed sm:px-4 py-2.5 w-full z-20 top-0 start-0 border-b" style="padding-left: 10%; padding-right: 10%;" color="green">
    <NavBrand href="/">
      <img src="/android-chrome-512x512.png" class="me-3 h-6 sm:h-9" alt="My Profile" />
      <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Pierce</span>
    </NavBrand>
    <NavHamburger color="indigo" />
    <NavUl>
      <NavLi href="/">Home</NavLi>
      <NavLi href="/about">About</NavLi>
      <NavLi href="/idk">Idk</NavLi>
      <NavLi href="https://piercew.xyz/">Misc</NavLi>
    </NavUl>
    <NavUl>
      {#if window.innerWidth < 768}
      {#each profiles as [name, icon, link]}
      <NavLi href={link} target="_blank">
        <table><tbody><tr>
          <td>
            <img src={icon} class="me-3 h-6 sm:h-9" alt="{name} logo">
          </td>
          <td>
            {name}
          </td>
          </tr></tbody></table>
      </NavLi>
      {/each}
      {:else}
      {#each profiles as [name, icon, link]}
      <NavLi href={link} target="_blank">
        <img src={icon} class="me-3 h-6 sm:h-9" alt="{name} logo" />
      </NavLi>
      {/each}
      {/if}
    </NavUl>
  </Navbar>
</div>

<main class="container md:container">

{@render children()}

<div style="height:5000px;" class="overflow-scroll pb-16">
  <Skeleton divClass="mt-16 mb-8" />
  <ImagePlaceholder divClass="my-8" />
  <TextPlaceholder divClass="my-8" />
</div>

</main>

<!--
<nav style="position: fixed;">
	<a href="/">home</a>
	<a href="/about">about</a>
</nav>
-->
