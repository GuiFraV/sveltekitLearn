<script lang="ts">

    import Fizzbuzz from "$lib/Fizzbuzz.svelte";
    const numberList = [52,12,465,6,6,6,6,8,8,95,5,9,6];

</script>

<Fizzbuzz numberList={numberList}>
    <p>Hello Fizz</p>
</Fizzbuzz>

<style>

</style>