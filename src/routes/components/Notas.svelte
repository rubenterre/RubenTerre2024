<script>
	import { onMount } from 'svelte';

	export let noticias = [
		{
			img: 'RadioGalega_noticia.png',
			tag: 'Entrevista en A vivir Galicia',
			date: '01 Enero 2017',
			name: 'Programa de "A vivir Galicia"',
			description: 'Entrevista en el espacio “Coñecer Galicia” sobre los vikingos en Galicia.',
			url: 'http://www.crtvg.es/rg/a-carta/conecer-galicia-conecer-galicia-do-dia-21-01-2017-2650682'
		},
		{
			img: 'LaVozDeGalicia1_noticia.png',
			tag: 'Curso de verano USC',
			date: '07 Junio 2015',
			name: 'Curso de verano USC',
			description:
				'Ponencia en el curso “Arte, Xeografía e Historia na Comarca do Salnés” en Vilanova de Arousa.',
			url: 'https://www.lavozdegalicia.es/noticia/arousa/catoira/2016/07/12/span-langgle-unha-pena-pegada-dos-vikingos-non-explotespan/0003_201607A12C11991.html'
		},
		{
			img: 'FarodeVigo_2015.png',
			tag: 'Entrevista Faro de Vigo',
			date: '11 Noviembre 2015',
			name: 'Entrevista para Faro de Vigo',
			description:
				'Sobre los vikingos en Galicia con motivo de la presentación del libro "Os viquingos na Comarca do Salnés".',
			url: 'http://www.farodevigo.es/portada-arousa/2016/07/11/ruben-terre-ria-arousa-puerta/1496290.html'
		},
		{
			img: 'CanalRiasBaixas_ruben_terre.png',
			tag: 'Presentación del libro',
			date: '12 Julio 2016',
			name: 'Presentación en Canal Rías Baixas',
			description:
				'El Pazo de Vista Real profundiza en la vida medieval y en las invasiones de los vikingos por la ría de Arousa<',
			url: 'http://www.canalriasbaixas.com/index.php/cultura/item/19894-a-mancomunidade-aposta-polo-pasado-vikingo-do-salnes-como-atractivo-cultural-e-turistico'
		},
		{
			img: 'FarodeVigo__presemtacion2016.png',
			tag: 'Presentación del libro',
			date: '11 Julio 2016',
			name: 'Presentación del libro en Cambados',
			description:
				'Un libro que analiza la presencia de los hombres del norte en la comarca do Salnés y los conflictos derivados.',
			url: 'http://www.diariodearousa.com/articulo/o-salnes/mancomunidade-explota-rastro-vikingos-salnes-favor-turismo/20151105232304127988.html'
		},
		{
			img: 'LaVozGalicia_Salnes.png',
			tag: 'Artículo en La Voz de Galicia',
			date: '11 Julio 2016',
			name: 'Artículo en La Voz de Galicia',
			description:
				'Un libro recoge la huella que dejaron los pueblos del norte en la comarca do Salnés y en parte del resto de Galicia.',
			url: 'https://www.lavozdegalicia.es/noticia/arousa/vilagarcia-de-arousa/2015/11/06/salnes-saca-partido-vikingos/0003_201511A6C5999.html'
		}
	];
</script>

{#each noticias as noticia}
	<div class="noticias__card">
		<img class="noticias__img" src="./blog/{noticia.img}" alt={noticia.name} />
		<h3 class="noticias__h3">{noticia.tag}</h3>
		<p class="noticias__fecha">{noticia.date}</p>
		<h4 class="noticias__h4">{noticia.name}</h4>
		<p class="noticias__p">{noticia.description}</p>
		<a href={noticia.url} class="noticias__a">Ver más ></a>
	</div>
{/each}

<style>
	.noticias__card {
		display: flex;
		flex-direction: column;
		/* flex: 0 0 50%; */
		width: 294px;
		margin: 10px;
		background: var(--white);
		border-radius: 12px;
		box-shadow: 0 5px 15px rgba(0, 0, 0, 15%);
		scroll-snap-align: start;
		transition: all 0.2s;
		background: #171819;
		border: 1px solid #979797;
		border-radius: 8px;
	}

	.noticias__img {
		border-radius: 8px;
		width: 294px;
		padding-bottom: 10px;
	}

	.noticias__h3 {
		font-size: 0.8rem;
		font-family: var(--fuente-principal);
		color: var(--color-principal);
		padding: 10px 20px 10px 20px;
	}

	.noticias__fecha {
		font-size: 0.7rem;
		font-family: var(--fuente-principal);
		color: var(--color-principal);
		padding: 0px 20px 10px 20px;
	}

	.noticias__h4 {
		font-size: 1rem;
		font-family: var(--fuente-principal);
		color: var(--color-principal);
		padding: 0px 20px 10px 20px;
	}

	.noticias__p {
		font-size: 0.9rem;
		font-family: var(--fuente-principal);
		color: var(--color-principal);
		padding: 0px 20px 10px 20px;
	}

	.noticias__a {
		font-size: 0.9rem;
		font-family: var(--fuente-principal);
		color: var(--color-cuaternario);
		padding: 0px 20px 25px 20px;
	}
</style>
