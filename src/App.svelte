<script>
  let people = [
    { name: "yoshi", beltColour: "black", age: 20, id: 1 },
	{ name: "mario", beltColour: "red", age: 30, id: 2 },
	{ name: "luigi", beltColour: "green", age: 40, id: 3 },
  ];
</script>

<main>
	<div>
		<h4>{people[0].name}</h4>
		<p>{people[0].beltColour}</p>
	</div>
	<div>
		<h4>{people[1].name}</h4>
		<p>{people[1].beltColour}</p>
	</div>
	<div>
		<h4>{people[2].name}</h4>
		<p>{people[2].beltColour}</p>
	</div>
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
