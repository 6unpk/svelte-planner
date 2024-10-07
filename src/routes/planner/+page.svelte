<script>
  import BackButton from '../../components/BackButton.svelte';
  import BigMenuButton from '../../components/BigMenuButton.svelte';
</script>

<svelte:head>
	<title>Planner</title>
	<meta name="description" content="Planner" />
</svelte:head>

<div class="">
	<div class="flex justify-center items-center h-screen">
		<div class="grid grid-cols-2 gap-4">
            <BigMenuButton label="앱 계획하기" bgColor="blue" hoverColor="blue" href="/planner/app" />
            <BigMenuButton label="게임 계획하기" bgColor="green" hoverColor="green" href="/planner/game" />
		</div>
	</div>
    <BackButton />
</div>
