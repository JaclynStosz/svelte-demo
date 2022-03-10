<script>
    import { name } from "../Stores/stores.js";
    import { createEventDispatcher } from "svelte";

    const dispatch = createEventDispatcher();
	const close = () => dispatch("close");

	let info;
</script>

<main>
    <div class="modal-bg" on:click={close}></div>
    <div class="modal" bind:this={info}>
        <h4>What is your name?</h4>
        <input bind:value={$name}/>
        <button on:click={close}>Ok</button>
    </div>
</main>

<style>
</style>