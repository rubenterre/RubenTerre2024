<script>
</script>

<section class="inicio">
	<div class="container">
		<div class="row">
			<div class="col s12 inicio__detalle">
				<img
					class="inicio__img"
					src="Ruben_Terre_img.webp"
					width="84px"
					alt="Retrato de Rubén Terré"
				/>
				<h1 class="inicio__h1">Hola, soy Rubén Terré 👋</h1>
				<h1 class="inicio__h1 inicio__h1--subtitulo">Diseño gráfico & web</h1>
				<div class="social">
					<a class="social__a" href="https://github.com/rubenterre"
						><div class="social__card">
							<img
								class="social__icon"
								src="icons/social/github_violeta.svg"
								alt="Github de Rubén Terré"
							/>
							<p class="social__p">Github</p>
						</div></a
					>
					<a class="social__a" href="https://www.linkedin.com/in/rubenterrelameiro/"
						><div class="social__card">
							<img
								class="social__icon"
								src="icons/social/linkedin_violeta.svg"
								alt="Github de Rubén Terré"
							/>
							<p class="social__p">Linkedin</p>
						</div></a
					>
					<a class="social__a" href="mailto:info@rubenterre.com"
						><div class="social__card">
							<img
								class="social__icon"
								src="icons/social/mail_violeta.svg"
								alt="Github de Rubén Terré"
							/>
							<p class="social__p">Email</p>
						</div></a
					>
				</div>

				<div class="perfil">
					<h2 class="perfil__h2">
						Soy Rubén Terré, desarrollador web, diseñador gráfico y docente.
					</h2>
					<p class="perfil__p">
						Como desarrollador web me dedico a ofrecer soluciones digitales a medida. Como diseñador
						gráfico puedo crear experiencias visuales personalizadas. Como docente, comparto mi
						pasión y conocimiento para formar a futuros profesionales. Explora mis proyectos y
						descubre cómo puedo ayudarte a llevar tus ideas al siguiente nivel. ¡Construyamos
						juntos!
					</p>
					<a
						href="Ruben_Arturo_Terre_Lameiro_CV2024.pdf"
						download="Descargar CV de Rubén Terré"
						class="perfil__a"
						><img src="./icons/descargar_icon.svg" alt="Botón de descarga de currículum" />DESCARGAR
						CV</a
					>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	.inicio {
		background: url('fondo_morphism1.png');
		background-position: center;
		background-size: contain;
		background-repeat: no-repeat;
	}

	.inicio__detalle {
		display: flex;
		justify-content: center;
		flex-direction: column;
		align-items: center;
		margin-top: 30px;
	}

	.inicio__h1 {
		margin-top: 20px;
		margin-bottom: 10px;
		font-size: 3rem;
		font-family: var(--fuente-principal);
		font-weight: 300;
	}

	.inicio__h1--subtitulo {
		margin-top: 0px;
		color: var(--color-secundario);
	}

	.social {
		display: flex;
		justify-content: space-evenly;
		width: 100%;
		margin: 30px 0px;
	}

	.social__card {
		display: flex;
		align-items: center;
		justify-content: space-evenly;
		border-radius: 12px;
		border: 1px solid rgba(92, 71, 224, 1);
		opacity: 1;
		background-color: rgba(23, 24, 25, 1);
		width: 150px;
		height: 45px;
	}

	.social__p {
		font-family: var(--fuente-principal);
		color: var(--color-principal);
	}

	.perfil {
		text-align: center;
		padding: 40px 10px;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	.perfil__h2 {
		font-family: var(--fuente-secundaria);
		color: var(--color-principal);
		font-size: 1.2rem;
	}

	.perfil__p {
		font-family: var(--fuente-principal);
		color: var(--color-principal);
		font-size: 0.9rem;
		margin: 20px 0px;
		font-weight: 400;
		line-height: 1.5rem;
	}

	.perfil__a {
		display: flex;
		align-items: center;
		justify-content: space-evenly;
		background: rgba(23, 24, 25, 0.44);
		border: 1px solid #f3f3f3;
		border-radius: 8px;
		font-family: var(--fuente-secundaria);
		font-size: 1rem;
		color: var(--color-principal);
		letter-spacing: 0;
		width: 305px;
		height: 47px;
		padding: 10px 40px;
	}

	@media screen and (max-width: 480px) {
		.inicio__h1 {
			font-size: 1.8rem;
		}

		.social {
			display: flex;
			flex-direction: row;
			align-items: center;
			justify-content: space-around;
			flex-wrap: wrap;
		}

		.social__card {
			margin: 10px 0px;
		}
	}
</style>
