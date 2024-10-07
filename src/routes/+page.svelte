<script>
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<div class="flex flex-col space-y-6">
		<a href="/planner" class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-4 px-8 rounded text-lg mx-auto block text-center">
			만들기
		</a>
		<a href="/signup" class="bg-blue-400 hover:bg-blue-500 text-white font-bold py-4 px-8 rounded text-lg mx-auto block text-center">
			회원가입
		</a>
		<a href="/login" class="bg-blue-300 hover:bg-blue-400 text-white font-bold py-4 px-8 rounded text-lg mx-auto block text-center">
			로그인
		</a>
	</div>
</section>

<style lang="postcss">
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	a {
		width: 300px;
	}
</style>
