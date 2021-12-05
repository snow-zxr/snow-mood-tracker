<script>
    export let date;
    export let mood;
    export let comment;
</script>

<button type="button" class="list-group-item list-group-item-action">
    <div class="d-flex w-100 justify-content-between lh-1">
   	 <h6 class="my-0">{date}</h6>

   	 {#if mood === 'Worst'}
   		 <span class="text-danger">{mood}</span>
   	 {:else if mood === 'Bad'}
   		 <span class="text-warning">{mood}</span>
   	 {:else if mood === 'Okay'}
   		 <span class="text-primary">{mood}</span>
   	 {:else if mood === 'Good'}
   		 <span class="text-info">{mood}</span>
   	 {:else if mood === 'Best'}
   		 <span class="text-success">{mood}</span>
   	 {/if}
    </div>
    <small class="text-muted">{comment}</small>
</button>