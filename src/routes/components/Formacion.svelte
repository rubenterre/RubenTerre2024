<script>
	import { onMount } from 'svelte';

	export let formaciones = [
		{
			icon: 'forga_white',
			name: 'CERT. PROF. DOCENCIA DE LA FP PARA EL EMPLEO',
			institution: 'FORGA Santiago',
			date: '2023-2024'
		},
		{
			icon: 'cec',
			name: 'CERT. PROF. DESARROLLO DE APLICACIONES CON TECNOLOGÍAS WEB',
			institution: 'Confederación de empresarios de Coruña',
			date: '2020'
		},
		{
			icon: 'afundacion',
			name: 'FP GM PREIMPRESIÓN DIGITAL',
			institution: 'Colegio Hogar Afundación',
			date: '2015 - 2017'
		},
		{
			icon: 'USC-Logo2',
			name: 'EXPERTO UNIV. EN GESTIÓN CULTURAL',
			institution: 'Universidade de Santiago de Compostela',
			date: '2014 - 2015'
		},
		{
			icon: 'USC-Logo2',
			name: 'MASTER OFICIAL ESTUDOS MEDIEVAIS EUROPEOS',
			institution: 'Universidade de Santiago de Compostela',
			date: '2012 - 2013'
		},
		{
			icon: 'USC-Logo2',
			name: 'LICENCIATURA EN HISTORIA',
			institution: 'Universidade de Santiago de Compostela',
			date: '2006 - 2012'
		}
	];

	onMount(() => {
		console.log('Componente montado');
	});
</script>

<section class="formacion">
	<div class="container">
		<div class="row">
			<div class="col s12">
				<div class="main__titulares">
					<h3 class="main__h3">FORMACIÓN</h3>
					<p class="main__p">Estos son mis estudios y otras formaciones complementarias</p>
					<div class="main__linea"></div>
				</div>
				<div class="formacion__cards">
					{#each formaciones as formacion}
						<div class="formacion__card">
							<div class="formacion__logo">
								<img
									src="logos/{formacion.icon}.svg"
									alt={formacion.name}
									class="formacion__icon"
								/>
							</div>
							<div class="formacion__detalle">
								<h3 class="formacion__h3">
									{formacion.name}
								</h3>
								<p class="formacion__profesion">
									{formacion.institution}
								</p>
								<p class="formacion__fecha">
									{formacion.date}
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

.formacion{
	margin: 60px 0px;
}

	.formacion__cards {
		margin: 20px 0px;
        display: flex;
        gap: 15px;
        flex-direction: column;
	}

	.formacion__card {
		display: flex;
		align-items: center;
		border-radius: 8px;
		border: 1px solid rgba(151, 151, 151, 1);
		background-color: rgba(23, 24, 25, 1);
		padding: 20px;
	}

	.formacion__logo {
		padding: 20px;
	}

	.formacion__logo img {
		width: 120px;
        max-height: 50px;
	}

	.formacion__detalle {
		padding: 0px 30px;
	}

	.formacion__h3 {
		font-family: var(--fuente-secundaria);
		color: var(--color-principal);
		font-size: 1rem;
	}

	.formacion__profesion {
		font-family: var(--fuente-secundaria);
		color: var(--color-principal);
		font-size: 0.8rem;
		padding: 10px 0px;
	}

	.formacion__fecha {
		font-family: var(--fuente-secundaria);
		color: var(--color-principal);
		font-size: 0.7rem;
		font-weight: 300;
		font-style: italic;
	}

	.formacion__p {
		font-family: var(--fuente-secundaria);
		color: var(--color-principal);
		font-size: 1rem;
		padding-top: 10px;
		line-height: normal;
	}

	@media screen and (max-width: 480px) {
		.formacion__card {
			padding: 10px;
			display: flex;
			flex-direction: column;
		}

		.formacion__detalle {
			padding: 10px;
			display: flex;
			align-items: center;
			justify-content: center;
			flex-direction: column;
			margin-bottom: 20px;
		}

		.formacion__h3 {
			font-family: var(--fuente-secundaria);
			color: var(--color-principal);
			font-size: 0.9rem;
		}

		.formacion__p {
			font-size: 0.9rem;
			padding: 10px 10px;
			text-align: center;
		}
	}
</style>
