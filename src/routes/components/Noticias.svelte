<script>
	import Notas from "./Notas.svelte";

	
</script>

<div class="noticias">
	<div class="noticias__cards">
    <Notas></Notas>
	</div>
</div>

<style>

	.noticias__cards {
    display: flex;
  padding: 25px 0px;
  list-style: none;
  overflow-x: scroll;
  scroll-snap-type: x mandatory;
	}
	.noticias__cards::-webkit-scrollbar {
  height: 12px;
}

.noticias__cards::-webkit-scrollbar-thumb,
.noticias__cards::-webkit-scrollbar-track {
  border-radius: 92px;
}

.noticias__cards::-webkit-scrollbar-thumb {
  background: var(--color-principal);
}

.noticias__cards::-webkit-scrollbar-track {
  background: var(--color-fondo);
}
</style>
