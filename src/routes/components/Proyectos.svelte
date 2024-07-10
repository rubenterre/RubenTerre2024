<script>
	import { onMount } from 'svelte';

	export let proyectos = [
		{
			banner: 'GaliciaWeatherApp.webp',
			name: 'GaliciaWeather App',
			description: 'Aplicación del tiempo con ilustraciones de ciudades de Galicia.',
			technologies: [
				`<img src="./icons/skills/svelte_icon.svg" alt="Svelte" width="20px">`,
				`<img src="./icons/skills/sketch_dark_icon.svg" alt="Sketch" width="20px">`
			],
			url: 'https://www.behance.net/gallery/155847275/Galicia-Weather-App'
		},
		{
			banner: 'ADM_Comunicaciones.png',
			name: 'ADM Comunicaciones',
			description: 'Página web corporativa y tienda online.',
			technologies: [
				`<img src="./icons/skills/wordpress_icon.svg" alt="Wordpress" width="20px">`,
				`<img src="./icons/skills/photoshop_icon.svg" alt="Photoshop" width="20px">`
			],
			url: 'https://admcomunicaciones.com/'
		},
		{
			banner: 'SoloHistoria.png',
			name: 'SoloHistoria App',
			description: 'Aplicación para aprender historia medieval.',
			technologies: [
				`<img src="./icons/skills/html5_icon.svg" alt="HTML" width="20px">`,
				`<img src="./icons/skills/css_icon.svg" alt="CSS" width="20px">`,
				`<img src="./icons/skills/javascript_icon.svg" alt="JavaScript" width="20px">`,
				`<img src="./icons/skills/sketch_dark_icon.svg" alt="Sketch" width="20px">`
			],
			url: 'https://www.behance.net/gallery/97500747/SoloHistoria-App-Learning-history'
		},
		{
			banner: 'Museo_Pobo_Galego.png',
			name: 'Museo Pobo Galego',
			description: 'Concept da páxina web do Museo do Pobo Galego',
			technologies: [`<img src="./icons/skills/sketch_dark_icon.svg" alt="Sketch" width="20px">`],
			url: 'https://www.behance.net/gallery/92767455/Museo-do-Pobo-Galego-Web-Design-Concept'
		}
	];

	onMount(() => {
		console.log('Componente montado');
	});
</script>

<section class="proyectos">
	<div class="container">
		<div class="row">
			<div class="col s12">
				<div class="main__titulares">
					<h3 class="main__h3">PROYECTOS</h3>
					<p class="main__p">Algunos de mis proyectos</p>
					<div class="main__linea"></div>
				</div>
				<div class="proyectos__cards">
					{#each proyectos as proyecto}
						<div class="proyectos__card">
							<div class="proyectos__img">
								<img
									src="projects/{proyecto.banner}"
									alt={proyecto.name}
									class="proyectos__banner"
								/>
							</div>
							<div class="proyectos__detalles">
								<h4 class="proyectos__h4">
									{proyecto.name}
								</h4>
								<p class="proyectos__p">
									{proyecto.description}
								</p>
								<div class="proyectos__icons">
									{#each proyecto.technologies as technology}
										{@html technology}
									{/each}
								</div>
								<a href={proyecto.url} class="proyectos__a">Ver más ></a>
							</div>
						</div>
					{/each}
				</div>
				<div class="proyectos__info">
					<a href="" class="proyectos__trabajos">VER MÁS TRABAJOS</a>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	.proyectos {
		margin-top: 20px;
	}

	.proyectos__cards {
		display: flex;
		gap: 20px;
		flex-wrap: wrap;
		align-items: center;
		justify-content: center;
		margin-top: 30px;
	}

	.proyectos__card {
		display: flex;
		border-radius: 8px;
		border: 1px solid rgba(151, 151, 151, 1);
		background-color: rgba(23, 24, 25, 1);
		width: 451px;
		height: 193px;
	}

	.proyectos__detalles {
		padding: 20px;
		height: 100%;
		display: flex;
		flex-direction: column;
		justify-content: space-around;
	}

	.proyectos__banner {
		border-top-left-radius: 8px;
		border-bottom-left-radius: 8px;
	}

	.proyectos__h4 {
		font-family: var(--fuente-principal);
		font-size: 0.9rem;
		color: var(--color-principal);
		padding-bottom: 10px;
	}

	.proyectos__p {
		font-family: var(--fuente-principal);
		font-size: 0.8rem;
		color: var(--color-principal);
		padding-bottom: 10px;
	}

	.proyectos__icons {
		display: flex;
		align-items: center;
		justify-content: left;
		gap: 10px;
		margin-bottom: 20px;
	}

	.proyectos__a {
		font-family: var(--fuente-principal);
		color: var(--color-cuaternario);
		font-size: 1rem;
	}

	.proyectos__info {
		display: flex;
		align-items: center;
		justify-content: center;
		margin: 40px 0px;
	}

	.proyectos__trabajos {
		border-radius: 8px;
		border: 1px solid rgba(151, 151, 151, 1);
		background-color: rgba(45, 47, 51, 1);
		width: 177px;
		height: 28px;
		font-family: var(--fuente-principal);
		color: var(--color-principal);
		font-size: 0.8rem;
		text-align: center;
        padding: 5px 0px;
	}
</style>
