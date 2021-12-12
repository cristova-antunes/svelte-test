<script>
	import Page  from "./components/layout/page.svelte";
    import Btn from "./components/elements/button.svelte";

    const handleBtnClick = () => console.log('btn clicked');
</script>

<Page>
    <Btn on:click={handleBtnClick}>Teste</Btn>
</Page>

<style>
</style>