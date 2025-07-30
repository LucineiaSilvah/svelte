<script>
  import Router from 'svelte-spa-router';
	import Home from './pages/Home.svelte';
	import About from './pages/About.svelte';
 let name = '';

 let poema = `No começo era o HTML, tão puro e tão só,
CSS dançava, mas o JS dava nó.
Então veio o Svelte, leve como papel,
Sem virtual DOM, voa como um carrossel.

Com bind ele escuta o que o input diz,
E com #each a lista sorri, feliz.
export let faz o dado viajar,
De um componente para outro se transformar.

script no topo, o estilo abaixo,
Tudo no mesmo arquivo, sem qualquer atalho.
Sem mil dependências pra configurar,
Com um npm run dev, já começa a brilhar.

Reativo por natureza, suave como o vento,
Transforma seu código em puro encantamento.
Na simplicidade, esconde um poder sutil:
Criar interfaces de forma gentil.

Então ergue seu mouse, codadora gentil,
Com Svelte nos dedos, conquiste o Brasil.
Pois quem aprende Svelte, com carinho e paixão,
Planta interfaces e colhe solução.`
	let count = 0

	function incremento(){
		count ++;
	}


	const routes ={
		'/home':Home,
		'/about' : About
	};
</script>

<main>
	<h1 >
	App</h1>
   <p>'{poema}'</p>
 <!-- <button on:click={incremento}>
	click {count} x
 </button>


 {#if count >  5}
   <p>vc clicou bastante</p>
 {/if} -->
</main>
 <hr>
 <div>
<a href="#/home">Home</a>
<a href="#/about">About</a>

 </div>
<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}
	a{
		text-decoration: none;
		color: #ff3e00;
		font-weight: bold;
		padding-left: 1rem;
	}
	a:hover{
		color: #ec805c;
	}
p{
	color:#161312;
	font-style: italic;
}
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
<Router {routes}/>