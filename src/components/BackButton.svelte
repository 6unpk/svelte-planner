<script>
  import { goto } from '$app/navigation';

  function goBack() {
    history.back();
  }
</script>

<button
  on:click={goBack}
  class="fixed bottom-4 left-4 px-4 py-2 bg-gray-200 text-gray-700 rounded-lg hover:bg-gray-300 focus:outline-none focus:ring-2 focus:ring-gray-400"
>
  뒤로 가기
</button>
