<script>
	let { text, fn } = $props();
</script>

<button
	onclick={fn}
	class="m-2 rounded-xl border px-3 py-2 transition-all duration-200 hover:bg-black hover:text-white active:scale-110"
	>{text}</button
>
