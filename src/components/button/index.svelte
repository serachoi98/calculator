


<script lang="ts">
    export let text: string;
    export let onClick : (value: string)=> void;
    export let color : 'orange' | 'gray' | 'dark-grey';
</script>

<div class="button"
data-color={color}
on:click={() => onClick(text)}>{text}</div>

<style lang="scss">
    .button {
       width: 80px;
       height: 80px;
       display: flex;
       align-items: center;
       justify-content: center;
       font-size: 24px;

       &[data-color='orange']{
        background-color: rgb(193, 59, 144);
       } &[data-color='gray']{
        background-color: rgb(70, 57, 64);
       }
       &[data-color='dark-grey']{
        background-color: darkgray;
       }
    }
    </style>


<p> This <em> Awesome Calculator </em> is made by <em>Sera Choi! </em> um_haha~!! </p>