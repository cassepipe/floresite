<script>
	import '../app.css';
</script>

<!-- Top-right navigation -->
<nav class="absolute top-0 right-0 p-4 top-nav">
	<ul class="flex space-x-4">
		<li><a href="/cv.pdf" target="_blank" class="text-gray-800 hover:text-blue-500">CV</a></li>
		<li><a href="/contact" class="text-gray-800 hover:text-blue-500">Contact</a></li>
		<li><a href="/about" class="text-gray-800 hover:text-blue-500">A Propos</a></li>
	</ul>
</nav>

<div class="flex">
	<!-- Sidebar navigation -->
	<nav class="p-4 w-64 h-screen text-white bg-gray-800">
		<ul class="space-y-4">
			<li><a href="editions" class="hover:text-gray-300">Éditions</a></li>
			<li><a href="#" class="hover:text-gray-300">Installation</a></li>
			<li><a href="#" class="hover:text-gray-300">Projets collectifs</a></li>
			<li><a href="#" class="hover:text-gray-300">Performances</a></li>
		</ul>
	</nav>

	<!-- Main content slot -->
	<slot></slot>
</div>
