<script>
	import Button from '../../components/Button.svelte';
	import LoadingBar from '../../components/LoadingBar.svelte';
	import HorseRace from './HorseRace.svelte';
	let progress = $state(10);

	function increment() {
		if (progress <= 90) {
			progress += 10;
		}
	}

	function decrement() {
		if (progress >= 10) {
			progress -= 10;
		}
	}

	function reset() {
		progress = 0;
	}
</script>

<HorseRace />

<div class="bg-red-500 transition-all duration-1000 hover:bg-blue-500">Transition</div>

<div class="m-4 h-10 w-15 border bg-blue-300 transition-all duration-1000 hover:skew-x-30">
	Box 1
</div>
<div class="m-4 h-10 w-15 border bg-blue-300 transition-all duration-1000 hover:blur-sm">Box 2</div>
<div class="m-4 h-10 w-15 border bg-blue-300 transition-all duration-1000 hover:rotate-720">
	Box 3
</div>
<div class="m-4 h-10 w-15 border bg-blue-300 transition-all duration-1000 hover:scale-150">
	Box 4
</div>

<div class="m-4">
	<Button text={'Increment'} fn={increment} />
	<Button text={'Decrement'} fn={decrement} />
	<Button text={'Reset'} fn={reset} />
	<LoadingBar color={'bg-blue-500'} current={progress} max={100} />
</div>
