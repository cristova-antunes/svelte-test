<script>
	import Footer  from "./footer.svelte";

    export let pageTitle;
</script>


<div class="main-content">
    {#if pageTitle !== ""}
        <h1 class="page-title">{pageTitle}</h1>
    {/if}
    
    <slot></slot>
</div>
<Footer />

<style>

    .main-content {
        padding: var(--space-l) var(--space-m);
    }

    .page-title {
        font-size: 2rem;
        font-weight: bold;
        margin-bottom: var(--space-l);
    }

</style>