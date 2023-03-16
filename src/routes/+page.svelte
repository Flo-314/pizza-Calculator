<script>
	let cantidadDePizzas = 0;
	let tiempoDeLevado = 0;
	let temperaturaDelAmbiente = 0;

	$: harina = cantidadDePizzas * 250;
	$: agua = harina * 0.69;
	$: sal = harina * 0.02;
	$: aceite = harina * 0.02;
	$: queso = cantidadDePizzas * 250;
	$: levadura = (harina * 20) / 69 / tiempoDeLevado / temperaturaDelAmbiente;
</script>

<div>
	<h1>pizzas</h1>
	<p>
		cantidad de pizzas: <input type="text" bind:value={cantidadDePizzas} />
		tiempo de levadso (para el mismo dia) <input type="text" bind:value={tiempoDeLevado} />
		temperatura del ambiente<input type="text" bind:value={temperaturaDelAmbiente} />
	</p>

	<p>harina: {harina}</p>
	<p>agua: {agua}</p>
	<p>levadura seca : {levadura / 3} levadura fresca: {levadura}</p>
	<p>sal: {sal}</p>
	<p>aceite: {aceite}</p>
	<p>queso: {queso}</p>
</div>
