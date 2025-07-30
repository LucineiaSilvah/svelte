<script>
  import Router from 'svelte-spa-router';
	import Home from './pages/Home.svelte';
	import About from './pages/About.svelte';
 let name = '';
  
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
{name}
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

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
<Router {routes}/>