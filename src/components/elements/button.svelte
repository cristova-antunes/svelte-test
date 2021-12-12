<script>
    export let isPrincipal = true;
    export let disabled = false;

</script>

<button class="btn {isPrincipal ? "is--principal" : ""}" {disabled} on:click>
    <slot></slot>
</button>