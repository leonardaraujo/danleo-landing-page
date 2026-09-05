<script lang="ts">
	import { MapPin, MessageCircle } from '@lucide/svelte';
</script>

<svelte:head>
	<title>DANLEO | Ropa familiar</title>
	<meta name="description" content="Ropa familiar de calidad a precios accesibles." />
</svelte:head>

<section class="relative h-[calc(100vh-56px)] min-h-[560px] bg-gray-200">
	<div class="absolute inset-0"><img src="/home.jpg" alt="Colección DANLEO" class="h-full w-full object-cover" /></div>
	<div class="absolute inset-0 bg-black/20"></div>
	<div class="relative z-10 flex h-full items-center">
		<div class="mx-auto w-full max-w-7xl px-4">
			<div class="max-w-lg">
				<h1 class="caprasimo mb-4 text-5xl font-bold text-white sm:text-6xl">Todo Mujer</h1>
				<p class="mb-8 text-xl text-white">Hasta 50% dscto.</p>
				<a href="#catalogo" class="caprasimo inline-block border-2 border-white px-8 py-3 font-medium text-white transition hover:bg-white hover:text-black">VER COLECCIÓN</a>
			</div>
		</div>
	</div>
	<a href="#catalogo" class="absolute bottom-8 left-1/2 flex h-8 w-8 -translate-x-1/2 items-center justify-center rounded-full border-2 border-white text-white" aria-label="Ver novedades">↓</a>
</section>

<section id="catalogo" class="bg-gray-50 px-4 py-20">
	<div class="mx-auto max-w-3xl text-center">
		<h2 class="caprasimo mb-4 text-4xl font-bold text-danleo-verde">ÚLTIMAS NOVEDADES</h2>
		<p class="mb-10 text-lg text-gray-600">Calidad y precio para toda la familia</p>
		<div class="rounded-lg bg-white px-6 py-14 shadow-sm">
			<div class="mx-auto mb-5 flex h-16 w-16 items-center justify-center rounded-full bg-danleo-verde/10 text-3xl text-danleo-verde" aria-hidden="true">✦</div>
			<h3 class="caprasimo mb-3 text-2xl text-danleo-verde">Estamos preparando esta sección</h3>
			<p class="mx-auto max-w-xl text-gray-600">Muy pronto podrás descubrir nuestros productos y novedades. Estamos trabajando para ofrecerte la mejor experiencia.</p>
		</div>
	</div>
</section>

<section id="ubicacion" class="bg-white px-4 py-20" aria-labelledby="ubicacion-titulo">
	<div class="mx-auto max-w-7xl">
		<div class="mb-10 text-center">
			<p class="mb-3 text-sm font-bold uppercase tracking-[0.2em] text-danleo-naranja">Visítanos</p>
			<h2 id="ubicacion-titulo" class="caprasimo text-4xl font-bold text-danleo-verde">Ubícanos</h2>
			<p class="mt-3 text-lg text-gray-600">Encuéntranos en nuestra tienda de Huancayo</p>
		</div>
		<div class="grid overflow-hidden rounded-2xl border border-danleo-verde/10 bg-white shadow-[0_12px_35px_rgba(0,68,63,0.1)] md:grid-cols-[1.15fr_0.85fr]">
			<div class="min-h-[280px] bg-gray-100 md:min-h-[360px]">
				<iframe
					title="Ubicación de DANLEO en Google Maps"
					src="https://www.google.com/maps?q=-12.068642,-75.204142&z=17&output=embed"
					class="h-full min-h-[280px] w-full border-0 md:min-h-[360px]"
					loading="lazy"
					allowfullscreen
				></iframe>
			</div>
			<div class="flex flex-col justify-center p-8 sm:p-10">
				<div class="mb-5 flex h-14 w-14 items-center justify-center rounded-full bg-danleo-verde/10 text-danleo-verde"><MapPin class="h-7 w-7" /></div>
				<h3 class="caprasimo text-2xl text-danleo-verde">Nuestra tienda</h3>
				<p class="mt-3 leading-7 text-gray-600">Prolongación Ica, C.C. Santa Rosa, interior Tienda 13, primer piso.<br />Huancayo, Junín</p>
				<a href="https://maps.app.goo.gl/qdAW8YVbgtwNcV5F9" target="_blank" rel="noopener noreferrer" class="mt-7 inline-flex w-fit items-center gap-2 rounded-lg bg-danleo-verde px-5 py-3 font-bold text-white transition hover:bg-danleo-naranja">
					<MapPin class="h-5 w-5" />
					Abrir en Google Maps
				</a>
			</div>
		</div>
	</div>
</section>

<section id="contacto" class="bg-gray-50 px-4 py-20" aria-labelledby="contacto-titulo">
	<div class="mx-auto max-w-3xl">
		<div class="mb-10 text-center">
			<p class="mb-3 text-sm font-bold uppercase tracking-[0.2em] text-danleo-naranja">Estamos para ayudarte</p>
			<h2 id="contacto-titulo" class="caprasimo text-4xl font-bold text-danleo-verde">Contáctanos</h2>
			<p class="mt-3 text-lg text-gray-600">Escríbenos y te responderemos lo antes posible.</p>
		</div>
		<div class="overflow-hidden rounded-2xl bg-white shadow-[0_12px_35px_rgba(0,68,63,0.1)]">
			<div class="p-6 sm:p-10">
				<a href="https://wa.me/51938588279" target="_blank" rel="noopener noreferrer" class="contact-option group sm:mx-auto sm:max-w-md">
					<span class="contact-icon bg-[#00E676]/15 text-[#009b52]"><MessageCircle class="h-6 w-6" /></span>
					<span><strong class="block text-lg text-danleo-verde">WhatsApp</strong><span class="mt-1 block text-slate-600 group-hover:text-danleo-naranja">+51 938 588 279</span></span>
				</a>
			</div>
		</div>
	</div>
</section>

<style>
	.caprasimo { font-family: 'Caprasimo', cursive; }
	.contact-option { display: flex; align-items: center; gap: 1rem; border: 1px solid #e2e8f0; border-radius: 0.75rem; padding: 1rem; transition: border-color 150ms, box-shadow 150ms; }
	.contact-option:hover { border-color: #ff7b00; box-shadow: 0 4px 12px rgb(0 68 63 / 0.08); }
	.contact-icon { display: flex; height: 3rem; width: 3rem; flex-shrink: 0; align-items: center; justify-content: center; border-radius: 9999px; background: rgb(0 68 63 / 0.1); color: #00443f; }
</style>
