<script>
	import Button from '../../components/Button.svelte';
</script>

<div class="w-full bg-blue-200">
	<div class="prose p-5">
		<h1 class="text-center text-blue-900">Aiden's Profile</h1>

		<hr />

		<div
			class="profile-image h-20 w-20 overflow-hidden rounded-full bg-black bg-cover bg-center"
		></div>
		<div>Aiden Akbarpour</div>
		<div>Student</div>

		<h2 class="text-center text-blue-900">About Me</h2>

		<p class="text-center">Hi, my name is Aiden.</p>

		<h2 class="text-center text-blue-900">Haiku Exercise</h2>
		<div class="bg-red-300 text-center">Warm, fresh, scented air,</div>
		<div class="bg-orange-300 text-center">Alive with springtime's essence,</div>
		<div class="bg-yellow-300 text-center">Hail summer's approach.</div>

		<h2 class="text-center text-blue-900">Components</h2>

		<Button text={'Click me!'} message={'Ok'} />
		<Button text={"Don't click me!"} message={'Why did you click me?'} />
	</div>
</div>

<style>
	.profile-image {
		background-image: url('https://images.unsplash.com/photo-1530281700549-e82e7bf110d6?q=80&w=688&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
	}
</style>
