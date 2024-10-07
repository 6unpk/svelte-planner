<script>
	import BackButton from '../../../../components/BackButton.svelte';
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div>
	<div class="bg-white p-8 rounded-lg shadow-lg w-full max-w-4xl mx-auto h-screen flex flex-col">
		<input type="text" placeholder="제목을 입력하세요" class="w-full text-2xl font-bold mb-4 p-2 border-b-2 border-gray-300 focus:outline-none focus:border-blue-500">
		<textarea placeholder="내용을 입력하세요" class="w-full p-2 border-2 border-gray-300 rounded focus:outline-none focus:border-blue-500 flex-grow"></textarea>
	</div>
	<BackButton />
</div>

<style lang="postcss">
	textarea {
		height: 100%;
		resize: none;
	}
</style>