<script>
	import { onMount } from 'svelte';

	export let experiencias = [
		{
			icon: 'ap-logo-blanco-medium-1',
			name: 'Grupo Academia Postal',
			profession: 'Profesor titular',
			date: '2023-2024',
			description:
				'Docencia de certificados de profesionalidad relacionados con desarrollo web y IT de sistemas microinformáticos.'
		},
		{
			icon: 'RT_logo',
			name: 'Freelance',
			profession: 'Desarrollador front-end',
			date: '2022-2023',
			description:
				'Desarrollo, mantenimiento y actualización de páginas web corporativas, blogs…'
		},
		{
			icon: 'ADM-500x133_blanco',
			name: 'ADM Comunicaciones',
			profession: 'Desarrollador & diseñador',
			date: '2018-2019',
			description:
				'Diseñador gráfico y maquetador web. Creación de web de empresa y papelería publicitaria y corporativa.'
		},
		{
			icon: 'INVBIT_LOGOTIPO',
			name: ' INVBIT',
			profession: 'Diseñador gráfico & maquetador',
			date: '2017 - 2018',
			description:
				'Diseñador gráfico y maquetador web. Creación de páginas web y e-commerce (Wordpress...).'
		}
	];

	onMount(() => {
		console.log('Componente montado');
	});
</script>

<section class="experiencia">
	<div class="container">
		<div class="row">
			<div class="col s12">
				<div class="main__titulares">
					<h3 class="main__h3">EXPERIENCIA</h3>
					<p class="main__p">Estos son algunas de mis experiencias profesionales</p>
					<div class="main__linea"></div>
				</div>
				<div class="experiencia__cards">
					{#each experiencias as experiencia}
						<div class="experiencia__card">
							<div class="experiencia__logo">
								<img
									src="logos/{experiencia.icon}.svg"
									alt={experiencia.name}
									class="experiencia__icon"
								/>
							</div>
							<div class="experiencia__detalle">
								<h3 class="experiencia__h3">
									{experiencia.name}
								</h3>
								<p class="experiencia__profesion">
									{experiencia.profession}
								</p>
								<p class="experiencia__fecha">
									{experiencia.date}
								</p>
                                <p class="experiencia__p">
									{experiencia.description}
								</p>

							</div>
						</div>
					{/each}
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	.experiencia__cards {
		margin: 20px 0px;
        display: flex;
        gap: 15px;
        flex-direction: column;
	}

	.experiencia__card {
		display: flex;
		align-items: center;
		border-radius: 8px;
		border: 1px solid rgba(151, 151, 151, 1);
		background-color: rgba(23, 24, 25, 1);
		padding: 20px;
	}

	.experiencia__logo {
		padding: 20px;
	}

	.experiencia__logo img {
		width: 120px;
        max-height: 50px;
	}

	.experiencia__detalle {
		padding: 0px 30px;
	}

	.experiencia__h3 {
		font-family: var(--fuente-secundaria);
		color: var(--color-principal);
		font-size: 1rem;
	}

	.experiencia__profesion {
		font-family: var(--fuente-secundaria);
		color: var(--color-principal);
		font-size: 0.8rem;
		padding: 10px 0px;
	}

	.experiencia__fecha {
		font-family: var(--fuente-secundaria);
		color: var(--color-principal);
		font-size: 0.7rem;
		font-weight: 300;
		font-style: italic;
	}

	.experiencia__p {
		font-family: var(--fuente-secundaria);
		color: var(--color-principal);
		font-size: 1rem;
		padding-top: 10px;
        line-height: normal;
	}

	@media screen and (max-width: 480px) {
		.experiencia__card {
			padding: 10px;
			display: flex;
			flex-direction: column;
		}

		.experiencia__detalle {
			padding: 10px;
			display: flex;
			align-items: center;
			justify-content: center;
			flex-direction: column;
			margin-bottom: 20px;
		}

		.experiencia__h3 {
			font-family: var(--fuente-secundaria);
			color: var(--color-principal);
			font-size: 0.9rem;
		}

		.experiencia__p {
			font-size: 0.9rem;
			padding: 10px 10px;
			text-align: center;
		}
	}
</style>
