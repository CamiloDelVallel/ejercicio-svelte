<script>
	const movies = [
	  {
	    name: "Avengers",
	    available: 5,
	    quantity: 0
	  },
	  {
	    name: "Terminator",
	    available: 3,
	    quantity: 0
	  },
	  {
	    name: "Loki",
	    available: 9,
	    quantity: 0
	  },
	  {
	    name: "Cruela",
	    available: 2,
	    quantity: 0
	  }
	];
</script>

{#each movies as movie}

<form>
	<h3>{movie.name}</h3>

	<button type="button" on:click={() => movie.quantity -=1} disabled={movie.quantity<=0}>-</button>
	{movie.quantity}
	<button type="button" on:click={()=> movie.quantity +=1} disabled={movie.quantity>=movie.available}>+</button>
</form>
{/each}