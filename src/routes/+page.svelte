<script lang="ts">
	// =====================================================
	// DATOS DE LA PÁGINA
	// =====================================================

	const beneficios = [
		{
			icono: '💡',
			titulo: 'Comparte conocimiento',
			texto: 'Ofrece asesorías y comparte lo que sabes con otros estudiantes.',
			detalle:
				'En SkinsU puedes compartir los conocimientos que dominas y apoyar a otros estudiantes mediante asesorías entre compañeros.'
		},
		{
			icono: '📚',
			titulo: 'Encuentra apoyo',
			texto: 'Encuentra compañeros que pueden ayudarte con diferentes materias.',
			detalle:
				'Si necesitas apoyo en alguna materia, SkinsU busca facilitar que encuentres estudiantes que tengan conocimientos sobre ese tema.'
		},
		{
			icono: '🎮',
			titulo: 'Gana XP',
			texto: 'Participa, ayuda y acumula puntos de experiencia dentro de SkinsU.',
			detalle:
				'La propuesta incluye un sistema de experiencia. Al participar y ayudar a otros estudiantes puedes acumular XP y avanzar dentro de la plataforma.'
		},
		{
			icono: '🏆',
			titulo: 'Sube de nivel',
			texto: 'Obtén niveles, insignias y reconocimientos por tu participación.',
			detalle:
				'El sistema de progreso busca reconocer la participación de los estudiantes mediante niveles, insignias y posibles recompensas.'
		}
	];

	const pasos = [
		{
			numero: '01',
			titulo: 'Crea tu perfil',
			texto:
				'Indica qué conocimientos puedes compartir y en qué temas necesitas apoyo.',
			detalle:
				'El estudiante podrá crear un perfil donde indique los conocimientos que puede compartir y también los temas en los que necesita apoyo académico.'
		},
		{
			numero: '02',
			titulo: 'Conecta',
			texto:
				'Encuentra estudiantes que puedan ayudarte o compañeros a quienes puedas ayudar.',
			detalle:
				'SkinsU busca facilitar el encuentro entre estudiantes que necesitan apoyo y compañeros que tienen conocimientos que pueden compartir.'
		},
		{
			numero: '03',
			titulo: 'Comparte',
			texto:
				'Participa en asesorías y forma parte de una comunidad de aprendizaje.',
			detalle:
				'Después de conectar con otros estudiantes, puedes participar en asesorías y contribuir a una comunidad basada en el aprendizaje colaborativo.'
		}
	];

	// =====================================================
	// ESTADO DEL MODAL
	// =====================================================

	let modalAbierto = $state(false);

	let informacionModal = $state({
		titulo: '',
		texto: ''
	});

	// =====================================================
	// ABRIR MODAL
	// =====================================================

	function abrirModal(titulo: string, texto: string) {
		informacionModal = {
			titulo,
			texto
		};

		modalAbierto = true;
	}

	// =====================================================
	// CERRAR MODAL
	// =====================================================

	function cerrarModal() {
		modalAbierto = false;
	}
</script>

<svelte:head>
	<title>SkinsU | Donde aprender y compartir es fácil</title>

	<meta
		name="description"
		content="SkinsU conecta estudiantes para compartir conocimientos, recibir asesorías y aprender juntos."
	/>
</svelte:head>

<div class="pagina">

	<!-- =====================================================
	     BARRA DE NAVEGACIÓN
	     ===================================================== -->

	<header class="barra-navegacion">

		<div class="logo">
			<img
				src="/LogoSkinsU-removebg-preview.png"
				alt="Logo oficial de SkinsU"
			/>
		</div>

		<nav>
			<a href="#inicio">Inicio</a>
			<a href="#que-es">¿Qué es?</a>
			<a href="#como-funciona">¿Cómo funciona?</a>
			<a href="#recompensas">Recompensas</a>
		</nav>

		<a class="boton-navegacion" href="#proximamente">
			Próximamente
		</a>

	</header>


	<!-- =====================================================
	     SECCIÓN PRINCIPAL
	     ===================================================== -->

	<section class="principal" id="inicio">

		<div class="contenido-principal">

			<div class="etiqueta">
				<span>✦</span>
				APRENDIZAJE COLABORATIVO
			</div>

			<h1>
				Aprende.
				<span>Comparte.</span>
				Crece.
			</h1>

			<p class="texto-principal">
				Una nueva forma de conectar estudiantes para compartir
				conocimientos, encontrar apoyo académico y aprender juntos.
			</p>

			<div class="botones-principales">

				<a href="#que-es" class="boton-principal">
					Conoce SkinsU
					<span>→</span>
				</a>

				<a href="#como-funciona" class="boton-secundario">
					¿Cómo funciona?
				</a>

			</div>

			<div class="estadisticas-principales">

				<div>
					<strong>XP</strong>
					<span>Experiencia</span>
				</div>

				<div>
					<strong>LVL</strong>
					<span>Niveles</span>
				</div>

				<div>
					<strong>🏆</strong>
					<span>Insignias</span>
				</div>

			</div>

		</div>


		<!-- TARJETA VISUAL DEL PERFIL -->

		<div class="visual-principal">

			<div class="tarjeta-perfil">

				<div class="encabezado-tarjeta">

					<div class="avatar">
						S
					</div>

					<div class="informacion-perfil">
						<strong>Tu perfil</strong>
						<span>Estudiante SkinsU</span>
					</div>

					<div class="nivel">
						LVL 03
					</div>

				</div>


				<div class="experiencia">

					<div class="informacion-experiencia">
						<span>Experiencia</span>
						<strong>720 / 1000 XP</strong>
					</div>

					<div class="barra-experiencia">
						<div class="progreso"></div>
					</div>

				</div>


				<div class="habilidades">

					<span>💻 Programación</span>
					<span>📐 Matemáticas</span>
					<span>🧠 Bases de datos</span>

				</div>


				<div class="insignia">

					<div class="icono-insignia">
						🏆
					</div>

					<div class="informacion-insignia">
						<strong>Mentor destacado</strong>
						<span>Comparte tus conocimientos</span>
					</div>

				</div>

			</div>


			<!-- Elementos flotantes -->

			<div class="elemento-flotante flotante-uno">
				<span>+100 XP</span>
				<small>¡Nueva asesoría!</small>
			</div>

			<div class="elemento-flotante flotante-dos">
				<span>★</span>
				<small>Nueva insignia</small>
			</div>

		</div>

	</section>


	<!-- =====================================================
	     SECCIÓN ¿QUÉ ES SKINSU?
	     ===================================================== -->

	<section class="seccion que-es" id="que-es">

		<div class="titulo-seccion">

			<span class="numero-seccion">
				01
			</span>

			<div>

				<span class="mini-titulo">
					CONOCE SKINSU
				</span>

				<h2>
					¿Qué es <span>SkinsU</span>?
				</h2>

			</div>

		</div>


		<div class="contenido-que-es">

			<div class="texto-grande">

				<p>
					SkinsU es una propuesta de plataforma educativa enfocada
					en <strong>conectar estudiantes</strong> para facilitar
					el intercambio de conocimientos mediante asesorías
					entre compañeros.
				</p>

				<p>
					La idea es crear un espacio donde cada estudiante pueda
					<strong>aprender, compartir o hacer ambas cosas.</strong>
				</p>

			</div>


			<div class="problema">

				<div class="icono-problema">
					💡
				</div>

				<h3>
					El conocimiento está en nuestra universidad.
				</h3>

				<p>
					Hay estudiantes que necesitan apoyo y otros que tienen
					conocimientos que pueden compartir. SkinsU busca
					facilitar que puedan encontrarse.
				</p>

			</div>

		</div>

	</section>


	<!-- =====================================================
	     SECCIÓN ¿CÓMO FUNCIONA?
	     ===================================================== -->

	<section class="seccion funcionamiento" id="como-funciona">

		<div class="titulo-seccion centrado">

			<span class="numero-seccion">
				02
			</span>

			<div>

				<span class="mini-titulo">
					ASÍ DE FÁCIL
				</span>

				<h2>
					¿Cómo funciona?
				</h2>

			</div>

		</div>


		<div class="pasos">

			{#each pasos as paso}

				<button
					type="button"
					class="paso interactivo"
					onclick={() => abrirModal(paso.titulo, paso.detalle)}
				>

					<span class="numero-paso">
						{paso.numero}
					</span>

					<div class="linea-paso"></div>

					<h3>
						{paso.titulo}
					</h3>

					<p>
						{paso.texto}
					</p>

					<span class="ver-mas">
						Ver más →
					</span>

				</button>

			{/each}

		</div>

	</section>


	<!-- =====================================================
	     SECCIÓN BENEFICIOS
	     ===================================================== -->

	<section class="seccion beneficios">

		<div class="titulo-seccion">

			<span class="numero-seccion">
				03
			</span>

			<div>

				<span class="mini-titulo">
					¿POR QUÉ SKINSU?
				</span>

				<h2>
					Aprender también puede ser
					<span>divertido.</span>
				</h2>

			</div>

		</div>


		<div class="cuadricula-beneficios">

			{#each beneficios as beneficio}

				<button
					type="button"
					class="beneficio interactivo"
					onclick={() => abrirModal(beneficio.titulo, beneficio.detalle)}
				>

					<div class="icono-beneficio">
						{beneficio.icono}
					</div>

					<h3>
						{beneficio.titulo}
					</h3>

					<p>
						{beneficio.texto}
					</p>

					<span class="ver-mas">
						Ver más →
					</span>

				</button>

			{/each}

		</div>

	</section>


	<!-- =====================================================
	     SECCIÓN XP, NIVELES Y RECOMPENSAS
	     ===================================================== -->

	<section class="recompensas" id="recompensas">

		<div class="contenido-recompensas">

			<span class="mini-titulo">
				SISTEMA DE PROGRESO
			</span>

			<h2>
				Tu conocimiento
				<br />
				<span>también tiene valor.</span>
			</h2>

			<p>
				Participa en SkinsU, acumula XP y avanza de nivel
				mientras ayudas a otros estudiantes.
			</p>


			<div class="progreso-skinsu">

				<div class="elemento-progreso activo">

					<div class="circulo-progreso">
						XP
					</div>

					<span>
						Experiencia
					</span>

				</div>


				<div class="flecha-progreso">
					→
				</div>


				<div class="elemento-progreso activo">

					<div class="circulo-progreso">
						LVL
					</div>

					<span>
						Niveles
					</span>

				</div>


				<div class="flecha-progreso">
					→
				</div>


				<div class="elemento-progreso activo">

					<div class="circulo-progreso">
						★
					</div>

					<span>
						Insignias
					</span>

				</div>


				<div class="flecha-progreso">
					→
				</div>


				<div class="elemento-progreso">

					<div class="circulo-progreso">
						🎓
					</div>

					<span>
						Recompensas
					</span>

				</div>

			</div>


			<!-- Recompensas académicas -->

			<div class="nota-recompensa">

				<strong>
					🎓 Recompensas académicas
				</strong>

				<span>
					Posibles beneficios como liberación de servicio o
					créditos complementarios, sujetos a los lineamientos
					y autorización de la institución.
				</span>

			</div>

		</div>

	</section>


	<!-- =====================================================
	     LLAMADO FINAL
	     ===================================================== -->

	<section class="seccion-final" id="proximamente">

		<div class="contenido-final">

			<span class="mini-titulo">
				PRÓXIMAMENTE
			</span>

			<h2>
				Tu conocimiento
				<br />
				puede ayudar a alguien.
			</h2>

			<p>
				SkinsU: donde aprender y compartir es fácil.
			</p>


			<div class="etiqueta-proximamente">

				<span>
					🚀
				</span>

				<strong>
					SKINSU APP
				</strong>

				<span>
					MUY PRONTO
				</span>

			</div>

		</div>

	</section>


	<!-- =====================================================
	     PIE DE PÁGINA
	     ===================================================== -->

	<footer>

		<div class="logo">

			<img
				src="/LogoSkinsU-removebg-preview.png"
				alt="Logo oficial de SkinsU"
			/>

		</div>


		<p>
			Donde aprender y compartir es fácil.
		</p>


		<a
			class="instagram"
			href="https://www.instagram.com/skinsu_itesa/"
			target="_blank"
			rel="noopener noreferrer"
		>
			📸 @skinsu_itesa
		</a>


		<span class="copyright">
			Proyecto académico · Cultura Empresarial
		</span>

	</footer>


	<!-- =====================================================
	     MODAL DINÁMICO
	     ===================================================== -->

	{#if modalAbierto}

		<div class="modal-fondo">

			<div
				class="modal-contenido"
				role="dialog"
				aria-modal="true"
				aria-labelledby="titulo-modal"
				tabindex="-1"
			>

				<button
					type="button"
					class="boton-cerrar"
					aria-label="Cerrar ventana"
					onclick={cerrarModal}
				>
					×
				</button>

				<span class="mini-titulo">
					CONOCE MÁS
				</span>

				<h2 id="titulo-modal">
					{informacionModal.titulo}
				</h2>

				<p>
					{informacionModal.texto}
				</p>

				<button
					type="button"
					class="boton-modal"
					onclick={cerrarModal}
				>
					Entendido
				</button>

			</div>

		</div>

	{/if}

</div>


<!-- =========================================================
     ESTILOS DE LA PÁGINA
     ========================================================= -->

<style>

	/* ---------------------------------------------------------
	   CONFIGURACIÓN GENERAL
	   --------------------------------------------------------- */

	:global(*) {
		box-sizing: border-box;
		margin: 0;
		padding: 0;
	}

	:global(html) {
		scroll-behavior: smooth;
	}

	:global(body) {
		font-family:
			Inter,
			ui-sans-serif,
			system-ui,
			-apple-system,
			BlinkMacSystemFont,
			"Segoe UI",
			sans-serif;

		background: #07111f;
		color: #f5f7fb;
	}

	:global(a) {
		text-decoration: none;
		color: inherit;
	}


	/* ---------------------------------------------------------
	   CONTENEDOR PRINCIPAL
	   --------------------------------------------------------- */

	.pagina {
		overflow: hidden;
		background: #07111f;
	}


	/* ---------------------------------------------------------
	   BARRA DE NAVEGACIÓN
	   --------------------------------------------------------- */

	.barra-navegacion {

		height: 78px;

		padding: 0 7%;

		display: flex;

		align-items: center;

		justify-content: space-between;

		border-bottom: 1px solid rgba(255, 255, 255, 0.08);

		background: rgba(7, 17, 31, 0.94);

		position: sticky;

		top: 0;

		z-index: 100;

		backdrop-filter: blur(12px);
	}


	.logo {

		display: flex;

		align-items: center;
	}


	.logo img {

		width: 150px;

		height: auto;

		display: block;
	}


	.barra-navegacion nav {

		display: flex;

		gap: 30px;

		font-size: 0.9rem;

		color: #aeb8c8;
	}


	.barra-navegacion nav a {

		transition: 0.2s ease;
	}


	.barra-navegacion nav a:hover {

		color: white;
	}


	.boton-navegacion {

		padding: 11px 18px;

		border: 1px solid rgba(0, 212, 255, 0.5);

		border-radius: 10px;

		color: #00d4ff;

		font-size: 0.85rem;

		font-weight: 700;
	}


	/* ---------------------------------------------------------
	   SECCIÓN PRINCIPAL
	   --------------------------------------------------------- */

	.principal {

		min-height: 680px;

		padding: 90px 7%;

		display: grid;

		grid-template-columns: 1fr 0.9fr;

		align-items: center;

		gap: 60px;

		position: relative;

		background:

			radial-gradient(
				circle at 75% 45%,
				rgba(78, 91, 255, 0.2),
				transparent 30%
			),

			radial-gradient(
				circle at 20% 30%,
				rgba(0, 212, 255, 0.08),
				transparent 25%
			);
	}


	.contenido-principal {

		max-width: 650px;
	}


	.etiqueta {

		display: inline-flex;

		gap: 8px;

		align-items: center;

		padding: 8px 13px;

		border: 1px solid rgba(0, 212, 255, 0.25);

		border-radius: 30px;

		background: rgba(0, 212, 255, 0.06);

		margin-bottom: 25px;

		color: #00d4ff;

		font-size: 0.75rem;

		font-weight: 800;

		letter-spacing: 2px;
	}


	.principal h1 {

		font-size: clamp(3.5rem, 7vw, 6.5rem);

		line-height: 0.92;

		letter-spacing: -5px;

		margin-bottom: 28px;
	}


	.principal h1 span {

		display: block;

		background:
			linear-gradient(
				90deg,
				#6d5dfc,
				#00d4ff
			);

		-webkit-background-clip: text;

		color: transparent;
	}


	.texto-principal {

		max-width: 560px;

		color: #aeb8c8;

		font-size: 1.1rem;

		line-height: 1.7;
	}


	/* ---------------------------------------------------------
	   BOTONES PRINCIPALES
	   --------------------------------------------------------- */

	.botones-principales {

		display: flex;

		gap: 14px;

		margin-top: 35px;
	}


	.boton-principal,
	.boton-secundario {

		padding: 15px 22px;

		border-radius: 11px;

		font-weight: 800;

		font-size: 0.9rem;
	}


	.boton-principal {

		background:
			linear-gradient(
				90deg,
				#6d5dfc,
				#00aeea
			);
	}


	.boton-secundario {

		border: 1px solid rgba(255, 255, 255, 0.15);

		color: #d8deea;
	}


	/* ---------------------------------------------------------
	   ESTADÍSTICAS
	   --------------------------------------------------------- */

	.estadisticas-principales {

		display: flex;

		gap: 40px;

		margin-top: 50px;
	}


	.estadisticas-principales div {

		display: flex;

		flex-direction: column;

		gap: 4px;
	}


	.estadisticas-principales strong {

		font-size: 1.1rem;
	}


	.estadisticas-principales span {

		color: #778399;

		font-size: 0.72rem;
	}


	/* ---------------------------------------------------------
	   TARJETA DEL PERFIL
	   --------------------------------------------------------- */

	.visual-principal {

		position: relative;

		min-height: 450px;

		display: grid;

		place-items: center;
	}


	.tarjeta-perfil {

		width: min(100%, 430px);

		padding: 27px;

		border: 1px solid rgba(255, 255, 255, 0.13);

		border-radius: 24px;

		background: rgba(19, 31, 51, 0.92);

		box-shadow:
			0 30px 80px rgba(0, 0, 0, 0.35);

		transform: rotate(2deg);
	}


	.encabezado-tarjeta {

		display: flex;

		align-items: center;

		gap: 13px;
	}


	.avatar {

		width: 52px;

		height: 52px;

		border-radius: 16px;

		display: grid;

		place-items: center;

		font-size: 1.5rem;

		font-weight: 900;

		background:
			linear-gradient(
				135deg,
				#6d5dfc,
				#00d4ff
			);
	}


	.informacion-perfil {

		display: flex;

		flex-direction: column;

		gap: 4px;

		flex: 1;
	}


	.informacion-perfil span {

		color: #8290a7;

		font-size: 0.75rem;
	}


	.nivel {

		padding: 6px 9px;

		border-radius: 7px;

		background: rgba(0, 212, 255, 0.1);

		color: #00d4ff;

		font-size: 0.72rem;

		font-weight: 800;
	}


	.experiencia {

		margin-top: 30px;
	}


	.informacion-experiencia {

		display: flex;

		justify-content: space-between;

		font-size: 0.72rem;

		margin-bottom: 8px;
	}


	.informacion-experiencia span {

		color: #8190a6;
	}


	.barra-experiencia {

		height: 8px;

		border-radius: 20px;

		background: #27354b;

		overflow: hidden;
	}


	.progreso {

		width: 72%;

		height: 100%;

		background:
			linear-gradient(
				90deg,
				#6d5dfc,
				#00d4ff
			);
	}


	.habilidades {

		display: flex;

		flex-wrap: wrap;

		gap: 8px;

		margin-top: 24px;
	}


	.habilidades span {

		padding: 8px 10px;

		border-radius: 8px;

		background: #111f33;

		color: #b7c1d1;

		font-size: 0.7rem;
	}


	.insignia {

		margin-top: 25px;

		padding: 14px;

		display: flex;

		gap: 12px;

		align-items: center;

		border-radius: 14px;

		background:
			linear-gradient(
				135deg,
				rgba(109, 93, 252, 0.14),
				rgba(0, 212, 255, 0.07)
			);
	}


	.icono-insignia {

		font-size: 1.6rem;
	}


	.informacion-insignia {

		display: flex;

		flex-direction: column;

		gap: 3px;
	}


	.informacion-insignia span {

		color: #8190a6;

		font-size: 0.7rem;
	}


	.elemento-flotante {

		position: absolute;

		padding: 13px 17px;

		border: 1px solid rgba(255, 255, 255, 0.12);

		border-radius: 12px;

		background: #142238;

		box-shadow:
			0 20px 40px rgba(0, 0, 0, 0.25);

		display: flex;

		flex-direction: column;

		gap: 3px;
	}


	.elemento-flotante span {

		color: #00d4ff;

		font-weight: 900;
	}


	.elemento-flotante small {

		color: #8190a6;

		font-size: 0.65rem;
	}


	.flotante-uno {

		top: 65px;

		right: -10px;
	}


	.flotante-dos {

		bottom: 55px;

		left: 0;
	}


	/* ---------------------------------------------------------
	   SECCIONES GENERALES
	   --------------------------------------------------------- */

	.seccion {

		padding: 110px 7%;
	}


	.que-es {

		background: #0b1728;
	}


	.titulo-seccion {

		display: flex;

		align-items: flex-start;

		gap: 22px;

		margin-bottom: 60px;
	}


	.titulo-seccion.centrado {

		justify-content: center;

		text-align: center;
	}


	.numero-seccion {

		color: #6d5dfc;

		font-size: 0.85rem;

		font-weight: 900;

		padding-top: 4px;
	}


	.mini-titulo {

		color: #00d4ff;

		font-size: 0.75rem;

		font-weight: 800;

		letter-spacing: 2px;
	}


	.titulo-seccion h2 {

		font-size: clamp(2.2rem, 4vw, 3.7rem);

		letter-spacing: -2px;

		margin-top: 9px;
	}


	.titulo-seccion h2 span {

		color: #00d4ff;
	}


	/* ---------------------------------------------------------
	   ¿QUÉ ES SKINSU?
	   --------------------------------------------------------- */

	.contenido-que-es {

		max-width: 1100px;

		margin: auto;

		display: grid;

		grid-template-columns: 1.2fr 0.8fr;

		gap: 60px;

		align-items: center;
	}


	.texto-grande p {

		color: #b3bdcd;

		font-size: 1.25rem;

		line-height: 1.9;

		margin-bottom: 20px;
	}


	.problema {

		padding: 30px;

		border-radius: 20px;

		background: #101f34;

		border: 1px solid rgba(255, 255, 255, 0.08);
	}


	.icono-problema {

		font-size: 2rem;

		margin-bottom: 18px;
	}


	.problema h3 {

		font-size: 1.4rem;

		margin-bottom: 12px;
	}


	.problema p {

		color: #8491a5;

		line-height: 1.7;

		font-size: 0.9rem;
	}


	/* ---------------------------------------------------------
	   ¿CÓMO FUNCIONA?
	   --------------------------------------------------------- */

	.pasos {

		max-width: 1100px;

		margin: auto;

		display: grid;

		grid-template-columns: repeat(3, 1fr);

		gap: 25px;
	}


	.paso {

		padding: 30px;

		border-radius: 20px;

		background: #0b1728;

		border: 1px solid rgba(255, 255, 255, 0.08);
	}


	.numero-paso {

		font-size: 2.8rem;

		font-weight: 900;

		color: #6d5dfc;
	}


	.linea-paso {

		width: 45px;

		height: 3px;

		background: #00d4ff;

		margin: 20px 0;
	}


	.paso h3 {

		font-size: 1.35rem;

		margin-bottom: 12px;
	}


	.paso p {

		color: #8491a5;

		line-height: 1.7;

		font-size: 0.9rem;
	}


	/* ---------------------------------------------------------
	   BOTONES INTERACTIVOS
	   --------------------------------------------------------- */

	.interactivo {

		appearance: none;

		-webkit-appearance: none;

		font-family: inherit;

		text-align: left;

		cursor: pointer;

		color: inherit;

		width: 100%;

		transition:
			transform 0.25s ease,
			border-color 0.25s ease,
			box-shadow 0.25s ease;
	}


	.interactivo:hover {

		transform: translateY(-7px);

		border-color: rgba(0, 212, 255, 0.45);

		box-shadow:
			0 15px 35px rgba(0, 0, 0, 0.25);
	}


	.interactivo:focus-visible {

		outline: 2px solid #00d4ff;

		outline-offset: 4px;
	}


	.ver-mas {

		display: block;

		margin-top: 20px;

		color: #00d4ff;

		font-size: 0.78rem;

		font-weight: 800;
	}


	/* ---------------------------------------------------------
	   BENEFICIOS
	   --------------------------------------------------------- */

	.beneficios {

		background: #0b1728;
	}


	.cuadricula-beneficios {

		max-width: 1100px;

		margin: auto;

		display: grid;

		grid-template-columns: repeat(4, 1fr);

		gap: 18px;
	}


	.beneficio {

		padding: 27px;

		border-radius: 18px;

		background: #101f34;

		border: 1px solid rgba(255, 255, 255, 0.07);
	}


	.icono-beneficio {

		font-size: 2rem;

		margin-bottom: 20px;
	}


	.beneficio h3 {

		margin-bottom: 10px;
	}


	.beneficio p {

		color: #8491a5;

		font-size: 0.85rem;

		line-height: 1.6;
	}


	/* ---------------------------------------------------------
	   RECOMPENSAS
	   --------------------------------------------------------- */

	.recompensas {

		padding: 120px 7%;

		background:

			radial-gradient(
				circle at 50% 0%,
				rgba(109, 93, 252, 0.18),
				transparent 35%
			),

			#07111f;

		text-align: center;
	}


	.contenido-recompensas {

		max-width: 1000px;

		margin: auto;
	}


	.recompensas h2 {

		font-size: clamp(2.5rem, 5vw, 4.5rem);

		line-height: 1;

		letter-spacing: -3px;

		margin: 15px 0 25px;
	}


	.recompensas h2 span {

		color: #00d4ff;
	}


	.recompensas p {

		color: #9ca8ba;

		max-width: 600px;

		margin: auto;

		line-height: 1.7;
	}


	.progreso-skinsu {

		display: flex;

		align-items: center;

		justify-content: center;

		gap: 20px;

		margin: 55px 0 35px;
	}


	.elemento-progreso {

		display: flex;

		flex-direction: column;

		align-items: center;

		gap: 9px;

		color: #718096;

		font-size: 0.75rem;
	}


	.elemento-progreso.activo {

		color: #dbe3ef;
	}


	.circulo-progreso {

		width: 62px;

		height: 62px;

		border-radius: 50%;

		display: grid;

		place-items: center;

		border: 1px solid #34445c;

		font-weight: 900;

		font-size: 0.75rem;
	}


	.elemento-progreso.activo .circulo-progreso {

		border-color: #6d5dfc;

		background: rgba(109, 93, 252, 0.12);

		color: #00d4ff;
	}


	.flecha-progreso {

		color: #536179;

		font-size: 1.4rem;
	}


	.nota-recompensa {

		max-width: 700px;

		margin: auto;

		padding: 20px;

		border: 1px solid rgba(0, 212, 255, 0.2);

		border-radius: 15px;

		background: rgba(0, 212, 255, 0.04);

		display: flex;

		flex-direction: column;

		gap: 8px;
	}


	.nota-recompensa strong {

		color: #00d4ff;
	}


	.nota-recompensa span {

		color: #8491a5;

		font-size: 0.8rem;

		line-height: 1.5;
	}


	/* ---------------------------------------------------------
	   SECCIÓN FINAL
	   --------------------------------------------------------- */

	.seccion-final {

		padding: 130px 7%;

		text-align: center;

		background: #0b1728;
	}


	.contenido-final h2 {

		font-size: clamp(3rem, 6vw, 5.8rem);

		line-height: 0.98;

		letter-spacing: -4px;

		margin: 18px 0;
	}


	.contenido-final p {

		color: #8e9bae;

		font-size: 1.1rem;
	}


	.etiqueta-proximamente {

		width: fit-content;

		margin: 35px auto 0;

		padding: 12px 18px;

		border-radius: 30px;

		display: flex;

		gap: 10px;

		align-items: center;

		background:
			linear-gradient(
				90deg,
				#6d5dfc,
				#00aeea
			);

		font-size: 0.75rem;

		font-weight: 900;

		letter-spacing: 1px;
	}


	/* ---------------------------------------------------------
	   PIE DE PÁGINA
	   --------------------------------------------------------- */

	footer {

		padding: 35px 7%;

		display: flex;

		align-items: center;

		justify-content: space-between;

		gap: 25px;

		border-top: 1px solid rgba(255, 255, 255, 0.07);

		color: #728097;

		font-size: 0.75rem;
	}


	footer .logo img {

		width: 125px;
	}


	.instagram {

		color: #00d4ff;

		font-weight: 700;

		transition: 0.2s ease;
	}


	.instagram:hover {

		color: #ffffff;

		transform: translateY(-2px);
	}


	.copyright {

		color: #566176;
	}


	/* ---------------------------------------------------------
	   MODAL
	   --------------------------------------------------------- */

	.modal-fondo {

		position: fixed;

		inset: 0;

		z-index: 1000;

		display: flex;

		align-items: center;

		justify-content: center;

		padding: 20px;

		background: rgba(0, 0, 0, 0.72);

		backdrop-filter: blur(8px);

		animation: aparecerFondo 0.2s ease;
	}


	.modal-contenido {

		position: relative;

		width: min(100%, 520px);

		padding: 40px;

		border: 1px solid rgba(0, 212, 255, 0.25);

		border-radius: 24px;

		background:
			linear-gradient(
				145deg,
				#142238,
				#0b1728
			);

		box-shadow:
			0 30px 80px rgba(0, 0, 0, 0.5);

		animation: aparecerModal 0.25s ease;
	}


	.modal-contenido h2 {

		margin: 12px 0 18px;

		font-size: 2rem;

		line-height: 1.1;
	}


	.modal-contenido p {

		color: #aeb8c8;

		font-size: 1rem;

		line-height: 1.8;
	}


	.boton-cerrar {

		position: absolute;

		top: 15px;

		right: 15px;

		width: 38px;

		height: 38px;

		border: 1px solid rgba(255, 255, 255, 0.1);

		border-radius: 50%;

		background: #101f34;

		color: white;

		font-size: 1.4rem;

		cursor: pointer;

		transition: 0.2s ease;
	}


	.boton-cerrar:hover {

		background: #6d5dfc;

		transform: rotate(90deg);
	}


	.boton-modal {

		margin-top: 28px;

		padding: 13px 22px;

		border: none;

		border-radius: 10px;

		background:
			linear-gradient(
				90deg,
				#6d5dfc,
				#00aeea
			);

		color: white;

		font-weight: 800;

		cursor: pointer;

		transition: 0.2s ease;
	}


	.boton-modal:hover {

		transform: translateY(-2px);

		box-shadow:
			0 8px 25px rgba(0, 174, 234, 0.25);
	}


	@keyframes aparecerFondo {

		from {
			opacity: 0;
		}

		to {
			opacity: 1;
		}
	}


	@keyframes aparecerModal {

		from {
			opacity: 0;

			transform: translateY(20px) scale(0.96);
		}

		to {
			opacity: 1;

			transform: translateY(0) scale(1);
		}
	}


	/* ---------------------------------------------------------
	   TABLETS
	   --------------------------------------------------------- */

	@media (max-width: 900px) {

		.barra-navegacion nav {

			display: none;
		}


		.principal {

			grid-template-columns: 1fr;

			padding-top: 60px;
		}


		.visual-principal {

			min-height: 400px;
		}


		.contenido-que-es {

			grid-template-columns: 1fr;
		}


		.cuadricula-beneficios {

			grid-template-columns: repeat(2, 1fr);
		}


		.pasos {

			grid-template-columns: 1fr;
		}

	}


	/* ---------------------------------------------------------
	   CELULARES
	   --------------------------------------------------------- */

	@media (max-width: 600px) {

		.barra-navegacion {

			padding: 0 5%;
		}


		.boton-navegacion {

			display: none;
		}


		.principal,
		.seccion,
		.recompensas,
		.seccion-final {

			padding-left: 5%;

			padding-right: 5%;
		}


		.logo img {

			width: 125px;
		}


		.principal h1 {

			font-size: 3.6rem;

			letter-spacing: -3px;
		}


		.botones-principales {

			flex-direction: column;
		}


		.estadisticas-principales {

			gap: 20px;
		}


		.tarjeta-perfil {

			transform: none;
		}


		.elemento-flotante {

			display: none;
		}


		.cuadricula-beneficios {

			grid-template-columns: 1fr;
		}


		.progreso-skinsu {

			flex-wrap: wrap;
		}


		.flecha-progreso {

			display: none;
		}


		footer {

			flex-direction: column;

			text-align: center;
		}


		footer .logo img {

			width: 125px;
		}


		.modal-contenido {

			padding: 32px 24px;
		}


		.modal-contenido h2 {

			font-size: 1.7rem;
		}

	}

</style>