<script>
  let people = [
    { name: "yoshi", beltColour: "black", age: 20, id: 1 },
	{ name: "mario", beltColour: "red", age: 30, id: 2 },
	{ name: "luigi", beltColour: "green", age: 40, id: 3 },
  ];

  const handleClick = (id) => {
	//delete the person from people
	people = people.filter((person) => person.id !== id);
  };
</script>

<main>
	{#each people as person (person.id)}
		<div>
			<h4>{person.name}</h4>
			<p>{person.age} years old, {person.beltColour} belt</p>
			<button on:click={() => handleClick(person.id)}>Delete</button>
		</div>
	{:else}
		<p>There are no people to show...</p>
	{/each}
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
