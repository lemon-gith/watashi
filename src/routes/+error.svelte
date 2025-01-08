<script lang="ts">
	import { page } from '$app/state';
</script>

{#if page.status == 404}
  <h1>Error 404</h1>
  <p>This is not the page you were looking for D:</p>
  <p>Please check the URL and try again :)</p>
{:else}
  <h1>
    {page.status}: {page.error ? page.error.message : "But error is null :0"}
  </h1>
{/if}
