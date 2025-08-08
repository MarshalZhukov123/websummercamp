<script>
	import { onMount } from 'svelte';
	import Button from '../../components/Button.svelte';
	let points = $state(0);
	let clickingPower = $state(1);
	let passiveIncome = $state(0);
	let clickUpgradeCost = 10;
	let passiveUpgradeCost = 50;

	let allTime = $state(0);
	let clickUpgradeNum = $state(0);
	let passiveUpgradeNum = $state(0);

	onMount(() => {
		let passiveTimer = setInterval(() => {
			points += passiveIncome;
		}, 1000);

		return () => clearInterval(passiveTimer);
	});

	function increment() {
		points += clickingPower;
		allTime += clickingPower;
	}

	function upgradeClickingPower(amount) {
		if (points - amount * clickUpgradeCost >= 0) {
			points -= amount * clickUpgradeCost;
			clickingPower += amount;
			clickUpgradeNum += amount;
		}
	}

	function upgradePassiveIncome(amount) {
		if (points - amount * passiveUpgradeCost >= 0) {
			points -= amount * passiveUpgradeCost;
			passiveIncome += amount;
			passiveUpgradeNum += amount;
		}
	}
</script>

<!-- Container for game -->
<div class="flex h-screen flex-col items-center justify-center bg-blue-300">
	<div>{points} points</div>
	<br />
	<button
		class="h-72 w-72 rounded-full bg-orange-400/60 transition-all duration-75 active:scale-110"
		onclick={increment}
	></button>
	<br />

	<!-- upgrades -->
	<div class="flex w-full border text-center">
		<div class=" w-1/2">
			<div class="text-xl">Clicker Upgrades</div>
			<Button text="+1 ({1 * clickUpgradeCost} points)" fn={() => upgradeClickingPower(1)} />
			<Button text="+5 ({5 * clickUpgradeCost} points)" fn={() => upgradeClickingPower(5)} />
			<Button text="+10 ({10 * clickUpgradeCost} points)" fn={() => upgradeClickingPower(10)} />
			<Button text="+50 ({50 * clickUpgradeCost} points)" fn={() => upgradeClickingPower(50)} />
			<Button
				text="+Max (+{parseInt(points / clickUpgradeCost)})"
				fn={() => upgradeClickingPower(points / clickUpgradeCost)}
			/>
		</div>
		<div class="w-1/2">
			<div class="text-xl">Passive Upgrades</div>
			<Button text="+1 ({1 * passiveUpgradeCost} points)" fn={() => upgradePassiveIncome(1)} />
			<Button text="+5 ({5 * passiveUpgradeCost} points)" fn={() => upgradePassiveIncome(1)} />
			<Button text="+10 ({10 * passiveUpgradeCost} points)" fn={() => upgradePassiveIncome(1)} />
			<Button text="+50 ({50 * passiveUpgradeCost} points)" fn={() => upgradePassiveIncome(1)} />
			<Button
				text="+Max (+{parseInt(points / passiveUpgradeCost)})"
				fn={() => upgradePassiveIncome(points / passiveUpgradeCost)}
			/>
		</div>
	</div>

	<!-- achievements and stats -->
	<div class="flex w-full border">
		<div class="w-1/2">
			<div class="text-center text-xl">Achievements</div>
			<div>Coming soon...</div>
		</div>
		<div class="w-1/2">
			<div class="text-center text-xl">Stats</div>
			<div>All-Time Points: {allTime}</div>
			<div>Clicker Upgrades Purchased: {clickUpgradeNum}</div>
			<div>Passive Income Upgrades Purchased: {passiveUpgradeNum}</div>
		</div>
	</div>
</div>
