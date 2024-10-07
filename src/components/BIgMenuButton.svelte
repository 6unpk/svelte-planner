<script>
    export let label = '';
    export let bgColor = 'blue';
    export let hoverColor = 'blue';
    export let href = '';
</script>

<a href={href} class="w-40 h-40 bg-{bgColor}-500 text-white text-xl font-bold rounded-lg shadow-lg hover:bg-{hoverColor}-600 transition duration-300">
    {label}
</a>

<style lang="postcss">
    a {
        width: 200px;
        height: 200px;
        display: flex;
        align-items: center;
        justify-content: center;
    }
</style>