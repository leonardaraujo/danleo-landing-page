<script lang="ts">
	import './layout.css';
	import { Phone, MapPin, Menu, X } from '@lucide/svelte';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
	let menuAbierto = $state(false);
	const telefono = '51938588279';

	function cerrarMenu() {
		menuAbierto = false;
	}
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
	<link href="https://fonts.googleapis.com/css2?family=Caprasimo&display=swap" rel="stylesheet" />
</svelte:head>

<div class="bg-danleo-verde py-2 text-center text-sm text-white">
	Visítanos en Prolongación Ica, C.C. Santa Rosa, interior Tienda 13 – 1.er piso. Huancayo,Junín
</div>

<header class="border-b border-danleo-verde/10 bg-white shadow-sm">
	<div class="mx-auto flex max-w-7xl items-center justify-between px-4 py-4">
		<a href="/" aria-label="Ir al inicio">
			<img src="/danleo_logo_orange.png" alt="DANLEO" class="h-10 w-auto" />
		</a>

		<nav class="hidden space-x-8 md:flex" aria-label="Navegación principal">
			<a href="/#contacto" class="nav-link">Contáctanos</a>
			<a href="/#ubicacion" class="nav-link">Ubícanos</a>
		</nav>

		<button
			class="flex h-10 w-10 items-center justify-center text-danleo-verde transition hover:text-danleo-naranja md:hidden"
			onclick={() => (menuAbierto = !menuAbierto)}
			aria-label={menuAbierto ? 'Cerrar menú' : 'Abrir menú'}
		>
			{#if menuAbierto}<X class="h-6 w-6" />{:else}<Menu class="h-6 w-6" />{/if}
		</button>
	</div>

	{#if menuAbierto}
		<nav class="border-t border-danleo-verde/10 bg-white px-4 py-4 md:hidden" aria-label="Menú móvil">
			<a href="/#contacto" class="mobile-link" onclick={cerrarMenu}>Contáctanos</a>
			<a href="/#ubicacion" class="mobile-link" onclick={cerrarMenu}>Ubícanos</a>
		</nav>
	{/if}
</header>

<main class="min-h-screen bg-white">{@render children()}</main>

<footer class="bg-danleo-verde">
	<div class="mx-auto max-w-7xl px-4 py-12">
		<div class="mb-8 grid grid-cols-1 gap-8 md:grid-cols-2">
			<div class="text-center md:text-left">
				<img src="/danleo_logo_orange.png" alt="DANLEO" class="mx-auto mb-4 h-8 w-auto brightness-0 invert md:mx-0" />
				<p class="mb-4 text-white/80">Ropa familiar de calidad a precios accesibles</p>
				<div class="flex justify-center space-x-4 md:justify-start">
					<a href="https://www.facebook.com/profile.php?id=100054511267583" target="_blank" rel="noopener noreferrer" class="social-link" aria-label="Facebook">
						<img src="/icons/facebook-icon.svg" alt="" class="h-6 w-6" />
					</a>
					<a href="https://www.tiktok.com/@danleo_huancayo" target="_blank" rel="noopener noreferrer" class="social-link" aria-label="TikTok">
						<img src="/icons/tiktok-icon-dark.svg" alt="" class="h-6 w-6" />
					</a>
				</div>
			</div>

			<div class="text-center md:text-left">
				<h2 class="mb-4 font-semibold text-white">Contacto</h2>
				<div class="space-y-3 text-white/80">
					<div class="flex items-center justify-center gap-2 md:justify-start"><Phone class="h-4 w-4 text-white/60" /><span>+51938588279</span></div>
					<div class="flex items-start justify-center gap-2 md:justify-start"><MapPin class="mt-1 h-4 w-4 shrink-0 text-white/60" /><span class="text-sm">Prolongación Ica Centro Comercial Santa Rosa interior Tienda 13 – 1.er piso<br />Huancayo, Junín</span></div>
				</div>
			</div>

		</div>
		<div class="border-t border-white/20 pt-6 text-center text-sm text-white/60">
			<p>RUC: 10415831396</p>
			<p>© 2026 DANLEO - Todos los derechos reservados</p>
		</div>
	</div>
</footer>

<a href={`https://wa.me/${telefono}`} target="_blank" rel="noopener noreferrer" class="fixed bottom-6 right-6 z-50 flex h-14 w-14 items-center justify-center rounded-full bg-[#00E676] shadow-lg transition hover:bg-[#00c95a]" aria-label="Contactar por WhatsApp">
	<img src="/whatsapp.svg" alt="WhatsApp" class="h-8 w-8" />
</a>

<style>
	:global(.nav-link) { color: #00443f; font-weight: 500; transition: color 150ms; }
	:global(.nav-link:hover) { color: #ff7b00; }
	:global(.mobile-link), :global(.footer-link) { display: block; padding: 0.5rem 0; }
	:global(.mobile-link) { color: #00443f; font-weight: 500; }
	:global(.footer-link) { color: white; }
	:global(.mobile-link:hover), :global(.footer-link:hover) { color: #ff7b00; }
	:global(.social-link) { display: flex; height: 2.5rem; width: 2.5rem; align-items: center; justify-content: center; border-radius: 9999px; background: rgb(255 255 255 / 0.1); color: white; transition: background 150ms; }
	:global(.social-link:hover) { background: rgb(255 255 255 / 0.2); }
</style>
