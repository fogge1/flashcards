<script lang="ts">
    
    let { question = "This is a question", explanation = "This is an explanation for a question"} = $props();
    let show_explanation = $state(false);

    function flip_card() {
        show_explanation = !show_explanation;
    }
</script>

<button 
class=flashcard
onclick={flip_card}
>
    {#if show_explanation}
        <p>{explanation}</p>
    {:else}
        <p>{question}</p>
    {/if}
</button>