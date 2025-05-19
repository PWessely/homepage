<script>
	import '../lib/styles/globals.css';
	import { page } from '$app/stores';
</script>

<div class="min-h-screen flex flex-col bg-gray-50 text-gray-900 font-sans">
	<!-- Navbar -->
	<header class="bg-white shadow-md sticky top-0 z-10">
		<div class="max-w-6xl mx-auto px-4 py-4 flex justify-between items-center">
			<h1 class="text-2xl font-bold text-blue-600">My Portfolio</h1>
			<nav class="space-x-6 text-lg">
				<a href="/" class="hover:text-blue-600 transition" class:font-semibold={$page.url.pathname === '/'}>Home</a>
				<a href="/projects" class="hover:text-blue-600 transition" class:font-semibold={$page.url.pathname.startsWith('/projects')}>Projects</a>
				<a href="/about" class="hover:text-blue-600 transition" class:font-semibold={$page.url.pathname.startsWith('/about')}>About</a>
				<a href="/contact" class="hover:text-blue-600 transition" class:font-semibold={$page.url.pathname.startsWith('/contact')}>Contact Me</a>
			</nav>
		</div>
	</header>

	<!-- Main content -->
	<main class="flex-grow max-w-6xl mx-auto w-full px-4 py-8">
		<slot />
	</main>

	<!-- Footer -->
	<footer class="bg-white border-t text-center text-sm text-gray-500 py-4">
		© {new Date().getFullYear()} Patrick Wessely. All rights reserved.
	</footer>
</div>
