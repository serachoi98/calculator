<script>
    import Screen from "./Screen.svelte";
    import Button from "./Button.svelte";
import { each } from "svelte/internal";

    const textNumbers = [
        ["7", "8", "9", "÷"],
        ["4", "5", "6", "*"],
        ["1", "2", "3", "-"],
        ["0", "C", "=", "+"],
    ];
    let result = "0";
</script>

<style>
    main {
       width: 80px;
       height: 80px;
       align-items: center;
       justify-content: center;
       font-size: 24px;
       background-color:palevioletred;  
    }
    .textNumber {
        display: flex;
    }
</style>

<main>
    <Screen {result} />
    <div class="keys">
        {#each textNumbers as textNumber}
        <div class="textNumber">
            {#each textNumber as key}
            <Button {key} bind:result />
            {/each}
            </div>
        {/each}
    </div>
</main>
