<script>
	import Horse from './Horse.svelte';
	import Button from '../../components/Button.svelte';
	let horses = $state([
		{
			emote: '🐎',
			position: 0,
			color: 'bg-red-300',
			animation: 'bounce'
		},
		{
			emote: '🐎',
			position: 0,
			color: 'bg-orange-300',
			animation: 'bounce'
		},
		{
			emote: '🐎',
			position: 0,
			color: 'bg-yellow-300',
			animation: 'bounce'
		},
		{
			emote: '🐎',
			position: 0,
			color: 'bg-green-300',
			animation: 'bounce'
		}
	]);

	function progress() {
		let maxHorse = horses[0];
		for (let horse of horses) {
			let r = parseInt(Math.random() * 20);
			horse.position += r;
			if (horse.position > 100) {
				horse.position = 100;
			}
			if (horse.position > maxHorse.position) {
				maxHorse = horse;
			}
		}

		for (let horse of horses) {
			if (horse.position == maxHorse.position) {
				horse.animation = 'spin';
			} else {
				horse.animation = 'bounce';
			}
		}
	}

	function reset() {
		for (let horse of horses) {
			horse.position = 0;
			horse.animation = 'bounce';
		}
	}
</script>

<div style="height: 400px;" class="bg-green-500">
	<div class="py-5 text-center text-2xl font-bold">HORSE RACING GAME</div>
	<Button text={'Gallop forward'} fn={progress} />
	<Button text={'Reset'} fn={reset} />

	<div class="py-10 pr-10">
		{#each horses as horse}
			<Horse
				emote={horse.emote}
				color={horse.color}
				animation={horse.animation}
				position={horse.position}
			/>
		{/each}
	</div>
</div>
