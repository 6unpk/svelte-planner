<script>
    import BackButton from '../../../components/BackButton.svelte';
    import BigMenuButton from '../../../components/BigMenuButton.svelte';
  </script>
  
  <svelte:head>
      <title>앱 계획하기</title>
      <meta name="description" content="앱 계획하기" />
  </svelte:head>
  
  <div class="text-column">
      <div class="absolute top-4 left-4 flex space-x-2">
          <button class="px-4 py-2 bg-blue-500 text-white text-sm font-semibold rounded-lg shadow hover:bg-blue-600 transition duration-300">
              컴퓨터에 저장
          </button>
          <button class="px-4 py-2 bg-green-500 text-white text-sm font-semibold rounded-lg shadow hover:bg-green-600 transition duration-300">
              불러오기
          </button>
          <button class="px-4 py-2 bg-purple-500 text-white text-sm font-semibold rounded-lg shadow hover:bg-purple-600 transition duration-300">
              계정으로 저장
          </button>
      </div>
      <div class="flex justify-center items-center h-screen">
          <div class="grid grid-cols-3 gap-4">
              <BigMenuButton label="아이디어" bgColor="blue" hoverColor="blue" />
              <BigMenuButton label="캐릭터" bgColor="green" hoverColor="green" />
              <BigMenuButton label="스토리" bgColor="yellow" hoverColor="yellow" />
              <BigMenuButton label="장르" bgColor="red" hoverColor="red" />
              <BigMenuButton label="목표" bgColor="purple" hoverColor="purple" />
          </div>
      </div>
      <BackButton />
  </div>
  