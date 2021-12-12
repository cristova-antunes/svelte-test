<script>
    import { createEventDispatcher } from 'svelte';

    const dispatch = createEventDispatcher();

	const forward = () => dispatch('img-click');
</script>

<header class="menu">
    <img src="https://via.placeholder.com/150" alt="Logo" class="menu__logo" on:click="{forward}">
    <nav class="menu__nav">
        <ul class="menu__list">
            <slot></slot>
        </ul>
    </nav>
</header>


<style>
    .menu {
        display: flex;
        align-items: center;
        padding-inline: var(--space-m);
        box-shadow: rgba(240, 46, 170, 0.4) 0px 5px,
                    rgba(240, 46, 170, 0.3) 0px 10px,
                    rgba(240, 46, 170, 0.2) 0px 15px,
                    rgba(240, 46, 170, 0.1) 0px 20px,
                    rgba(240, 46, 170, 0.05) 0px 25px;
    }

    .menu__logo {
        height: 80%;   
    }

    .menu__nav {
        flex: 1;   
    }

    .menu__list {
        display: flex;
        gap: var(--space-m);
        justify-content: flex-end;
    }
</style>