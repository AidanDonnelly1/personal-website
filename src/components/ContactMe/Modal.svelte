<script>
	import { setContext } from "svelte"
	import { isOpen, id } from "./store.js"
	const modalId = $$props.$$slots.default[0].name;
	setContext("modalId", modalId)
</script>

<div>
	<slot />
</div>

