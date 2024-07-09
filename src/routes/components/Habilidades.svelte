<script>
	import { onMount } from 'svelte';

	export let desarrollo = [
		{
			icon: 'html5_icon',
			name: 'HTML'
		},
		{
			icon: 'css_icon',
			name: 'CSS'
		},
		{
			icon: 'javascript_icon',
			name: 'JavaScript'
		},
		{
			icon: 'svelte_icon',
			name: 'Svelte'
		},
		{
			icon: 'bootstrap_icon',
			name: 'Bootstrap'
		},
		{
			icon: 'wordpress_icon',
			name: 'Wordpress'
		},
		{
			icon: 'github_icon',
			name: 'GitHub'
		}
	];

	onMount(() => {
		console.log('Componente montado');
	});
</script>

<section class="habilidades">
	<div class="container">
		<div class="row">
			<div class="col s12">
				<div class="main__titulares">
					<h3 class="main__h3">HABILIDADES</h3>
					<p class="main__p">Algunas de mis habilidades más destacadas</p>
					<div class="main__linea"></div>
				</div>
				<div class="habilidades__sections">
					<h3 class="habilidades__h3">▶︎ Desarrollo web</h3>
					<div class="habilidades__cards">
						{#each desarrollo as habilidad}
							<div class="habilidades__card">
								<img
									class="habilidades__icon"
									src="icons/skills/{habilidad.icon}.svg"
									alt={habilidad.name}
								/>
								<h4 class="habilidades__h4">{habilidad.name}</h4>
							</div>
						{/each}
					</div>
                    <h3 class="habilidades__h3">▶︎ Diseño gráfico</h3>
					<div class="habilidades__cards">
						{#each desarrollo as habilidad}
							<div class="habilidades__card">
								<img
									class="habilidades__icon"
									src="icons/skills/{habilidad.icon}.svg"
									alt={habilidad.name}
								/>
								<h4 class="habilidades__h4">{habilidad.name}</h4>
							</div>
						{/each}
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	.habilidades__sections {
		margin: 20px 0px;
	}

	.habilidades__h3 {
		margin: 20px 0px;
		color: var(--color-principal);
		font-family: var(--fuente-principal);
		font-size: 1rem;
	}

    .habilidades__cards{
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        justify-content: left;
        gap: 10px;
    }

	.habilidades__card {
		border-radius: 8px;
		border: 1px solid rgba(151, 151, 151, 1);
		background-color: rgba(23, 24, 25, 1);
        width: 220px;
        height: 82px;
        display: flex;
        align-items: center;
        justify-content: space-evenly;
	}

    .habilidades__icon{
        height: 39px;
    }
</style>
