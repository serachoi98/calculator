<script lang="ts">
    import {Button} from '@src/components/button';
    import { text } from 'svelte/internal';
    
    const textNumbers: string[]= ['1','2','3','4','5','6','7','8','9','0']
</script>

<div class="frame">
{#each textNumbers as text}
 <Button {text} color="orange" onClick={(value) => alert(value)} />
{/each}
</div>

<style lang="scss">
.frame{
    width: 240px;
    display: flex;
    flex-wrap: wrap;
}

</style>

<div>
    <Button text="1" onClick={() => {}} color="orange" />
</div>