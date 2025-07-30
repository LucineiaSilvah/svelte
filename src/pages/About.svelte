<script>
  import Card from "../components/Card.svelte";
  const title = 'About'
    let dados = [
    { titulo: "Aprender Svelte", descricao: "Estudar os fundamentos da framework." },
    { titulo: "Fazer projeto", descricao: "Criar um app com componentes e props." },
    { titulo: "Praticar", descricao: "Treinar todos os dias para fixar o conteúdo." }
  ];


</script>

<main>
  <h1>{title}</h1>
 {#each dados as item}
 <Card title={item.titulo} descricao={item.descricao}/>
{/each}

</main>