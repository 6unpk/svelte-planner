<svelte:head>
	<title>로그인</title>
	<meta name="description" content="로그인" />
</svelte:head>

<div>
<div class="flex flex-col items-center justify-center min-h-screen w-full">
  <div class="w-full max-w-md bg-white rounded-lg shadow-md p-8">
    <h2 class="text-3xl font-bold text-center mb-8">로그인</h2>
    <form class="space-y-6">
      <div>
        <label for="email" class="text-sm font-medium text-gray-700 block mb-2">이메일</label>
        <input type="email" id="email" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-500" placeholder="이메일을 입력하세요" required>
      </div>
      <div>
        <label for="password" class="text-sm font-medium text-gray-700 block mb-2">비밀번호</label>
        <input type="password" id="password" class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-500" placeholder="비밀번호를 입력하세요" required>
      </div>
      <div class="flex items-center justify-between mt-6">
        <a href="/signup" class="text-sm font-medium text-blue-600 hover:underline">
          회원가입
        </a>
		<button type="submit" class="px-6 py-3 bg-blue-600 text-white font-semibold rounded-lg shadow-md hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
			로그인
		  </button>  
      </div>
    </form>
  </div>
</div>
</div>
