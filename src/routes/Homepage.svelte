<script>
    import Page  from "../components/layout/inner-page.svelte";
    import Btn from "../components/elements/button.svelte";

    const handleBtnClick = () => console.log('btn clicked');
</script>

<Page pageTitle="Homepage">
    <Btn on:click={handleBtnClick}>Teste</Btn>
</Page>