<script>
    import Header  from "./header.svelte";
	import Footer  from "./footer.svelte";
</script>

<main>
    <Header />
    <div class="main-content">
        <slot></slot>
    </div>
    <Footer />
</main>

<style>
    main {
        height: 100%;
        display: grid;
        grid-template-rows: 80px 1fr 64px;
    }

    .main-content {
        padding: var(--space-l) var(--space-m);
    }

</style>