<script>
export let title;
export let descricao;
</script>
<div class="box">

  <div class="card">
    <h1>{title}</h1>
     <p>{descricao}</p>
  </div>
</div>

<style>
.box{
  width: 100%;
height: 50vh;
  display: flex;
  justify-content: center;
  align-items: center;


}
.card{
  border-radius: 1rem;
  width: 250px;
  padding: 2rem;
  margin: 1rem;
  border: 2px solid orangered;
}
</style>