<script>
    let data = new Promise((resolve, reject) => {
        reject(new Error("Some error"));
    });

    let session = null;
    setTimeout(() => {
        session = "mysessionid";
    }, 1000);
</script>
<!-- Notice that when removing the if, everything works as expected -->
{#if session != null}
    {#await data}
        Loading...
    {:then result}
        Got a result: {result}
    {:catch error}
        Caught an error: {error}
    {/await}
{/if}
