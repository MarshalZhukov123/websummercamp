<div class="relative h-screen bg-black bg-gradient-to-b from-black via-purple-900 to-black">
	<div class="flex justify-center text-2xl font-bold text-white">
		The Solar System (not to scale)
	</div>
	<div class=" flex justify-center text-white">
		On this model, 1 solar year is represented by 10 seconds. The rest of the orbits are timed
		accordingly.
	</div>
	<div class="absolute top-1/2 left-1/2 h-8 w-8 -translate-1/2 rounded-full bg-yellow-200"></div>

	<!-- mercury -->
	<div
		class="centered absolute h-12 w-12 animate-[spin_2.41s_linear_infinite]
		rounded-full border border-gray-200/40"
	>
		<div class="absolute h-2 w-2 translate-0.5 rounded-full bg-gray-300"></div>
	</div>

	<!-- venus -->
	<div
		class="centered absolute h-24 w-24 animate-[spin_6.15s_linear_infinite]
		rounded-full border border-gray-200/40"
	>
		<div class="absolute h-3 w-3 translate-2 rounded-full bg-orange-400"></div>
	</div>

	<!-- earth -->
	<div
		class="centered absolute h-36 w-36 animate-[spin_10s_linear_infinite]
		rounded-full border border-gray-200/40"
	>
		<div
			class="absolute h-3 w-3 translate-4 animate-[spin_0.808s_linear_infinite] rounded-full bg-gradient-to-b from-blue-300 via-blue-400 to-green-400"
		>
			<div class="h-1 w-1 -translate-[3px] rounded-full bg-white"></div>
		</div>
	</div>

	<!-- mars -->
	<div
		class="centered h-48 w-48 animate-[spin_18.8s_linear_infinite]
		rounded-full border border-gray-200/40"
	>
		<div
			class="absolute h-3 w-3 translate-5 rounded-full bg-gradient-to-b from-orange-400 via-orange-300 to-gray-100"
		></div>
	</div>

	<!-- jupiter -->
	<div
		class="centered h-84 w-84 animate-[spin_118.6s_linear_infinite]
		rounded-full border border-gray-200/40"
	>
		<div
			class="absolute h-10 w-10 translate-7 rounded-full bg-gradient-to-r from-orange-500 via-orange-200 to-red-500"
		></div>
	</div>

	<!-- saturn -->
	<div
		class="centered h-120 w-120 animate-[spin_290s_linear_infinite]
		rounded-full border border-gray-200/40"
	>
		<div class="absolute h-9 w-9 translate-12 rounded-full bg-yellow-200"></div>
	</div>

	<!-- uranus -->
	<div
		class="centered h-156 w-156 animate-[spin_840s_linear_infinite]
		rounded-full border border-gray-200/40"
	>
		<div class="absolute h-8 w-8 translate-18 rounded-full bg-blue-100"></div>
	</div>

	<!-- neptune -->
	<div
		class="centered h-192 w-192 animate-[spin_1650s_linear_infinite]
		rounded-full border border-gray-200/40"
	>
		<div
			class="absolute h-8 w-8 translate-24 rounded-full bg-gradient-to-r from-blue-500 via-blue-600 to-indigo-700"
		></div>
	</div>
</div>

<style>
	.centered {
		@apply absolute top-1/2 left-1/2 -translate-1/2 rounded-full;
	}
</style>
