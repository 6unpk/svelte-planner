<script lang="ts">
  import { writable } from 'svelte/store';

  const email = writable('');
  const password = writable('');
  const confirmPassword = writable('');
  const errorMessage = writable('');
  const username = writable('');
  function validateEmail(value: string) {
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    return emailRegex.test(value);
  }

  function handleSubmit() {
    if (!validateEmail($email)) {
      errorMessage.set('유효한 이메일 주소를 입력해주세요.');
      return;
    }

    if ($password.length < 8) {
      errorMessage.set('비밀번호는 8자 이상이어야 합니다.');
      return;
    }

    if ($password !== $confirmPassword) {
      errorMessage.set('비밀번호가 일치하지 않습니다.');
      return;
    }

    errorMessage.set('');
    // 여기에 회원가입 로직을 추가하세요
    console.log('회원가입 성공:', { email: $email, password: $password });
  }
</script>

<svelte:head>
	<title>회원 가입</title>
	<meta name="description" content="회원 가입" />
</svelte:head>

<div>
<div class="flex flex-col items-center justify-center min-h-screen">
  <div class="w-full max-w-md bg-white rounded-lg shadow-md p-8">
    <h2 class="text-3xl font-bold text-center mb-8">회원 가입</h2>
    <form class="space-y-6" on:submit|preventDefault={handleSubmit}>
      <div>
        <label for="email" class="text-sm font-medium text-gray-700 block mb-2">이메일</label>
        <input type="email" id="email" bind:value={$email} class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-500" placeholder="이메일을 입력하세요" required>
      </div>
      <div>
        <label for="username" class="text-sm font-medium text-gray-700 block mb-2">사용자 이름</label>
        <input type="text" id="username" bind:value={$username} class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-500" placeholder="사용자 이름을 입력하세요" required>
      </div>
      <div>
        <label for="password" class="text-sm font-medium text-gray-700 block mb-2">비밀번호</label>
        <input type="password" id="password" bind:value={$password} class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-500" placeholder="비밀번호를 입력하세요" required>
      </div>
      <div>
        <label for="confirmPassword" class="text-sm font-medium text-gray-700 block mb-2">비밀번호 확인</label>
        <input type="password" id="confirmPassword" bind:value={$confirmPassword} class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:outline-none focus:ring-2 focus:ring-blue-500" placeholder="비밀번호를 다시 입력하세요" required>
      </div>
      {#if $errorMessage}
        <p class="text-red-500 text-sm">{$errorMessage}</p>
      {/if}
      <div class="flex items-center justify-between mt-6">
        <button type="submit" class="px-6 py-3 bg-blue-600 text-white font-semibold rounded-lg shadow-md hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
          회원가입
        </button>
      </div>
    </form>
  </div>
</div>
</div>
