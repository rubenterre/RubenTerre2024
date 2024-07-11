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

	export let design = [
		{
			icon: 'indesign_icon',
			name: 'InDesign'
		},
		{
			icon: 'photoshop_icon',
			name: 'Photoshop'
		},
		{
			icon: 'illustrator_icon',
			name: 'Illustrator'
		},
		{
			icon: 'after-effects_icon',
			name: 'After Effects'
		},
		{
			icon: 'sketch_dark_icon',
			name: 'Sketch'
		},
		{
			icon: 'figma_icon',
			name: 'Figma'
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
					<h3 class="habilidades__h3">Desarrollo web</h3>
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
					<h3 class="habilidades__h3">Diseño gráfico</h3>
					<div class="habilidades__cards">
						{#each design as habilidad}
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
	.habilidades {
		margin: 50px 0px;
	}

	.habilidades__sections {
		margin: 20px 0px;
		display: flex;
		justify-content: center;
		flex-direction: column;
		align-items: center;
	}

	.habilidades__h3 {
		margin: 30px 0px;
		color: var(--color-principal);
		font-family: var(--fuente-principal);
		font-size: 1rem;
		text-decoration: underline;
	}

	.habilidades__cards {
		display: flex;
		flex-wrap: wrap;
		align-items: center;
		justify-content: center;
		gap: 10px;
	}
/* 
	.habilidades__card {
		border-radius: 8px;
		border: 1px solid rgba(151, 151, 151, 1);
		background-color: rgba(23, 24, 25, 1);
		width: 130px;
		height: 140px;
		display: flex;
		align-items: center;
		justify-content: space-evenly;
		flex-direction: column;
		position: relative;
		transform: scale(1, 1) translateZ(0px);
		transition-duration: 300ms;
		transition-property: transform, box-shadow;
		transition-timing-function: ease-out;
		-webkit-font-smoothing: subpixel-antialiased;
	}

	.habilidades__card:hover{
		box-shadow: rgba(0, 0, 0, 0.8) 0px 2px 58px -16px;
		transform: scale(1.05, 1.05) translateZ(0px) translate3d(0px, 0px, 0px);
		transition-duration: 300ms;
		transition-property: transform, box-shadow;
		transition-timing-function: ease-out;
		border-radius: 6px;
		border: 2px solid white;

	}

	.habilidades__icon {
		height: 39px;
		filter: brightness(0%) invert(1);
		transition: filter 0.3s;
	}

	.habilidades__icon:hover{
		filter: none;
	} */

</style>
