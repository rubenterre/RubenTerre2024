<script>
	import { onMount } from 'svelte';

	export let servicios = [
		{
			icon: 'code-bold_icon',
			name: 'DESARROLLO WEB',
			description: 'Codificación de sitios web, plataformas CMS …'
		},
		{
			icon: 'design-pencil_icon',
			name: 'DISEÑO GRÁFICO',
			description: 'En todo tipo de soportes:papel, pantallas…'
		},
		{
			icon: 'teacher_icon',
			name: 'DOCENCIA',
			description: 'Certificados de profesionalidad, cursos online….'
		}
	];

	onMount(() => {
		console.log('Componente montado');
	});
</script>

<section class="servicios">
	<div class="container">
		<div class="row">
			<div class="col s12">
				<div class="main__titulares">
					<h3 class="main__h3">MIS SERVICIOS</h3>
					<p class="main__p">Estas son algunas cosas que puedo hacer para ti:</p>
					<div class="main__linea"></div>
				</div>
				<div class="servicios__cards">
					{#each servicios as servicio}
						<div class="servicios__card">
							<img class="servicios__icon" src="icons/{servicio.icon}.svg" alt="{servicio.name}" />
							<h4 class="servicios__h4">{servicio.name}</h4>
							<p class="servicios__p">{servicio.description}</p>
						</div>
					{/each}
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	.servicios {
		margin: 30px 0px;
	}

	.servicios__cards {
		display: flex;
		margin: 30px 0px;
		flex-wrap: wrap;
		align-items: center;
		justify-content: space-around;
	}

	.servicios__card {
		border-radius: 8px;
		border: 1px solid rgba(151, 151, 151, 1);
		background-color: rgba(23, 24, 25, 1);
		padding: 10px 30px;
		width: 280px;
		height: 138px;
        margin: 10px 0px;
	}

	.servicios__icon {
		margin: 10px 0px;
	}

	.servicios__h4 {
		color: var(--color-principal);
		font-family: var(--fuente-principal);
		font-size: 1rem;
		font-weight: 400;
	}

    .servicios__p{
        color: var(--color-principal);
        font-family: var(--fuente-principal);
        font-size: .8rem;
        padding-top: 8px;
    }
</style>
