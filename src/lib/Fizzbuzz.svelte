<script lang="ts">

    export let numberList:Array<number>;
    
    let newNumber: number = 0;

    function addNumber(newNumber: number){
        numberList = [...numberList, newNumber];
        newNumber = 0
    }



</script>

<h2>FizzBuzz</h2>

<slot/>

{#each numberList as number}
    {#if number % 3 === 0 && number % 5 === 0}
        <p>Fizzbuzz</p>
    {:else if number % 3 === 0}
        <p>fizz</p>
    {:else if number % 5 === 0}
        <p>buzz</p>
    {:else}
        <p>{number}</p>
    {/if}
{/each}

<form>
    <input type="number" bind:value="{newNumber}">
    <button type="button" on:click={() => addNumber(newNumber)}>Ajouter</button>
</form>


<style>

</style>