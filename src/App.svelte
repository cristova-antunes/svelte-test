<script>
    import Header from "./components/layout/header.svelte";

    import {
        Router,
        navigate,
        Route,
        Link
    } from "svelte-navigator";
    import Homepage from "./routes/Homepage.svelte";
    import About from "./routes/About.svelte";
    import Contact from "./routes/Contact.svelte";

    const handleHeaderImgClick = () => navigate("/", { replace: true });
</script>

<Router>
    <main>
        <Header on:img-click={handleHeaderImgClick}>
            <Link to="About">About</Link>
            <Link to="Contact">Contact</Link>
        </Header>

        <Route>
            <Homepage />
        </Route>
        <Route path="About">
            <About />
        </Route>
        <Route path="Contact">
            <Contact />
        </Route>
    </main>
</Router>


<style>
    main {
        height: 100%;
        display: grid;
        grid-template-rows: 80px 1fr 64px;
    }
</style>