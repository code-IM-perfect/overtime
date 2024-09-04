<script>
	import '../app.css';
	import '../form.css'
	import Navbar from '../components/+Navbar.svelte';
	import Footer from '../components/+Footer.svelte';
	// import Task from '../components/+Task.svelte';
</script>

<div>
	<Navbar />
	<slot />
	<Footer />
	<!-- <Task /> -->
	
</div>
