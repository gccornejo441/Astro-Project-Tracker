<script>
    let count = 0;
    $: doubled = count *2;

    const incrementCount = () => {
        count += 1;
    };

    $: {
        console.log('count changed to ' + count);
    }

</script>

<button
    on:click={incrementCount}
    type="button"
    class="rounded-lg border border-primary-500 bg-primary-500 px-5 py-2.5 text-center text-sm font-medium text-white shadow-sm transition-all hover:border-primary-700 hover:bg-primary-700 focus:ring focus:ring-primary-200 disabled:cursor-not-allowed disabled:border-primary-300 disabled:bg-primary-300"
  >
    Clicked {count} {count === 1 ? 'time' : 'times'}
  </button>

  <p>{count} double is {doubled}</p>