<script lang="ts">
	let { children } = $props();
</script>
<!--
<div class="relative px-8">
  <Navbar class="px-2 sm:px-4 py-2.5 fixed w-full z-20 top-0 start-0 border-b">
    <NavBrand href="/">
      <img src="/android-chrome-512x512.png" class="me-3 h-6 sm:h-9" alt="My Profile" />
      <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">Pierce</span>
    </NavBrand>
    <NavHamburger />
    <NavUl>
      <NavLi href="/">Home</NavLi>
      <NavLi href="/about">About</NavLi>
      <NavLi href="/pricing">Pricing</NavLi>
      <NavLi href="/contact">Contact</NavLi>
    </NavUl>
  </Navbar>
  <div style="height:300px;" class="overflow-scroll pb-16">
    <Skeleton divClass="mt-16 mb-8" />
    <ImagePlaceholder divClass="my-8" />
    <TextPlaceholder divClass="my-8" />
  </div>
</div>-->

<nav>
	<a href="/">home</a>
	<a href="/about">about</a>
</nav>

{@render children()}

