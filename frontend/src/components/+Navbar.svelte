<script lang="ts">
	let links = [
		{ name: 'Home', url: '/' },
		{ name: 'About Us', url: '/about' },
		{ name: 'Admin Login', url: '/admin' },
		{ name: 'Worker Register', url: '/worker/register' },
	];
</script>

<nav class="flex justify-between content-center items-center text-white sm:mx-7">
	<h2 class="text-2xl font-extrabold p-4 mx-3">
		<a href="/" class="logo hover:opacity-90">
			<span id="o" class="logoChar">O</span>
			<span id="v" class="logoChar">v</span>
			<span id="e" class="logoChar">e</span>
			<span id="r" class="logoChar">r</span>
			<span id="t" class="logoChar">t</span>
			<span id="i" class="logoChar">i</span>
			<span id="m" class="logoChar">m</span>
			<span id="e" class="logoChar">e</span>
			</a>
	</h2>
	<ul class="flex justify-between">
		{#each links as link}
			<li class="navLink text-sm md:text-lg flex items-center inset-1">
				<a href={link.url} class="p-5">{link.name}</a>
			</li>
		{/each}
	</ul>
</nav>

 <style>
	.imgGlow {
		box-shadow: 0 0px 9px 1px rgba(255, 255, 255, 0.5);
	} 

	/* .logoChar {
		display: inline-block;
		animation-duration: 3.5s;
		animation-timing-function: ease-out;
		animation-iteration-count: 1;
	} */


	.logo:hover #o {
		animation-name: o;
	}
	.logo:hover #v {
		animation-name: v;
	}
	.logo:hover #e {
		animation-name: e;
	}
	.logo:hover #r {
		animation-name: r;
	}
	.logo:hover #t {
		animation-name: t;
	}
	.logo:hover #i {
		animation-name: i;
	}
	.logo:hover #m {
		animation-name: m;
	}
	.logo:hover #e {
		animation-name: e;
	}

	@keyframes o {
		0% {
			rotate: 0deg;
			animation-timing-function: cubic-bezier(0.19, 1, 0.22, 1);
		}
		13% {
			rotate: 380deg;
		}
		15% {
			translate: -300%;
			scale: 0.3;
			rotate: 380deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		20% {
			rotate: 360deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		30% {
			scale: 1;
			translate: -10%;
		}
		31% {
			scale: 0.6 1.4;
			translate: 40%;
		}
		35% {
			scale: 1.4 0.8;
			translate: -30%;
		}

		40% {
			scale: 0.8 1.2;
			translate: 20%;
		}
		45% {
			scale: 1.1 0.9;
			translate: -20%;
		}
		/* 50% {
			scale: 0.9 1.1;
			translate: 20%;
		} */
		50% {
			scale: 1;
			translate: 0;
		}
		100% {
			rotate: calc(360deg);
		}
	}
	@keyframes v {
		0% {
			rotate: 0deg;
			animation-timing-function: cubic-bezier(0.19, 1, 0.22, 1);
		}
		13% {
			rotate: 380deg;
		}
		15% {
			translate: -150%;
			scale: 0.3;
			rotate: 380deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		20% {
			rotate: 360deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		30% {
			scale: 1;
			translate: -10%;
		}
		31% {
			scale: 0.7 1.3;
			translate: 40%;
		}
		35% {
			scale: 1.3 0.9;
			translate: -30%;
		}

		40% {
			scale: 0.9 1.1;
			translate: 20%;
		}
		45% {
			scale: 1.05 0.95;
			translate: -20%;
		}
		/* 50% {
			scale: 0.9 1.1;
			translate: 20%;
		} */
		50% {
			scale: 1;
			translate: 0;
		}
		100% {
			rotate: calc(360deg);
		}
	}
	@keyframes e {
		0% {
			rotate: 0deg;
			animation-timing-function: cubic-bezier(0.19, 1, 0.22, 1);
		}
		13% {
			rotate: 380deg;
		}
		15% {
			translate: 300%;
			scale: 0.3;
			rotate: 380deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		20% {
			rotate: 360deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		30% {
			scale: 1;
			translate: 10%;
		}
		31% {
			scale: 0.6 1.4;
			translate: -40%;
		}
		35% {
			scale: 1.4 0.8;
			translate: 30%;
		}

		40% {
			scale: 0.8 1.2;
			translate: -20%;
		}
		45% {
			scale: 1.1 0.9;
			translate: 20%;
		}
		/* 50% {
			scale: 0.9 1.1;
			translate: 20%;
		} */
		50% {
			scale: 1;
			translate: 0;
		}
		100% {
			rotate: calc(360deg);
		}
	}
	@keyframes r {
		0% {
			rotate: 0deg;
			animation-timing-function: cubic-bezier(0.19, 1, 0.22, 1);
		}
		13% {
			rotate: 380deg;
		}
		15% {
			translate: 150%;
			scale: 0.3;
			rotate: 380deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		20% {
			rotate: 360deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		30% {
			scale: 1;
			translate: 10%;
		}
		31% {
			scale: 0.7 1.3;
			translate: -20%;
		}
		35% {
			scale: 1.3 0.9;
			translate: 15%;
		}

		40% {
			scale: 0.9 1.1;
			translate: -10%;
		}
		45% {
			scale: 1.05 0.95;
			translate: 10%;
		}
		/* 50% {
			scale: 0.9 1.1;
			translate: 20%;
		} */
		50% {
			scale: 1;
			translate: 0;
		}
		100% {
			rotate: calc(360deg);
		}
	}
	@keyframes t {
		0% {
			rotate: 0deg;
			animation-timing-function: cubic-bezier(0.19, 1, 0.22, 1);
		}
		13% {
			rotate: 380deg;
		}
		15% {
			translate: 150%;
			scale: 0.3;
			rotate: 380deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		20% {
			rotate: 360deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		30% {
			scale: 1;
			translate: 10%;
		}
		31% {
			scale: 0.7 1.3;
			translate: -20%;
		}
		35% {
			scale: 1.3 0.9;
			translate: 15%;
		}

		40% {
			scale: 0.9 1.1;
			translate: -10%;
		}
		45% {
			scale: 1.05 0.95;
			translate: 10%;
		}
		/* 50% {
			scale: 0.9 1.1;
			translate: 20%;
		} */
		50% {
			scale: 1;
			translate: 0;
		}
		100% {
			rotate: calc(360deg);
		}
	}

	@keyframes t {
		0% {
			rotate: 0deg;
			animation-timing-function: cubic-bezier(0.19, 1, 0.22, 1);
		}
		13% {
			rotate: 380deg;
		}
		15% {
			translate: 150%;
			scale: 0.3;
			rotate: 380deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		20% {
			rotate: 360deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		30% {
			scale: 1;
			translate: 10%;
		}
		31% {
			scale: 0.7 1.3;
			translate: -20%;
		}
		35% {
			scale: 1.3 0.9;
			translate: 15%;
		}

		40% {
			scale: 0.9 1.1;
			translate: -10%;
		}
		45% {
			scale: 1.05 0.95;
			translate: 10%;
		}
		/* 50% {
			scale: 0.9 1.1;
			translate: 20%;
		} */
		50% {
			scale: 1;
			translate: 0;
		}
		100% {
			rotate: calc(360deg);
		}
	}

	@keyframes i {
		0% {
			rotate: 0deg;
			animation-timing-function: cubic-bezier(0.19, 1, 0.22, 1);
		}
		13% {
			rotate: 380deg;
		}
		15% {
			translate: 150%;
			scale: 0.3;
			rotate: 380deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		20% {
			rotate: 360deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		30% {
			scale: 1;
			translate: 10%;
		}
		31% {
			scale: 0.7 1.3;
			translate: -20%;
		}
		35% {
			scale: 1.3 0.9;
			translate: 15%;
		}

		40% {
			scale: 0.9 1.1;
			translate: -10%;
		}
		45% {
			scale: 1.05 0.95;
			translate: 10%;
		}
		/* 50% {
			scale: 0.9 1.1;
			translate: 20%;
		} */
		50% {
			scale: 1;
			translate: 0;
		}
		100% {
			rotate: calc(360deg);
		}
	}

	@keyframes m {
		0% {
			rotate: 0deg;
			animation-timing-function: cubic-bezier(0.19, 1, 0.22, 1);
		}
		13% {
			rotate: 380deg;
		}
		15% {
			translate: 150%;
			scale: 0.3;
			rotate: 380deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		20% {
			rotate: 360deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		30% {
			scale: 1;
			translate: 10%;
		}
		31% {
			scale: 0.7 1.3;
			translate: -20%;
		}
		35% {
			scale: 1.3 0.9;
			translate: 15%;
		}

		40% {
			scale: 0.9 1.1;
			translate: -10%;
		}
		45% {
			scale: 1.05 0.95;
			translate: 10%;
		}
		/* 50% {
			scale: 0.9 1.1;
			translate: 20%;
		} */
		50% {
			scale: 1;
			translate: 0;
		}
		100% {
			rotate: calc(360deg);
		}
	}

	@keyframes e {
		0% {
			rotate: 0deg;
			animation-timing-function: cubic-bezier(0.19, 1, 0.22, 1);
		}
		13% {
			rotate: 380deg;
		}
		15% {
			translate: 150%;
			scale: 0.3;
			rotate: 380deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		20% {
			rotate: 360deg;
			animation-timing-function: cubic-bezier(0.95, 0.05, 0.795, 0.035);
		}
		30% {
			scale: 1;
			translate: 10%;
		}
		31% {
			scale: 0.7 1.3;
			translate: -20%;
		}
		35% {
			scale: 1.3 0.9;
			translate: 15%;
		}

		40% {
			scale: 0.9 1.1;
			translate: -10%;
		}
		45% {
			scale: 1.05 0.95;
			translate: 10%;
		}
		/* 50% {
			scale: 0.9 1.1;
			translate: 20%;
		} */
		50% {
			scale: 1;
			translate: 0;
		}
		100% {
			rotate: calc(360deg);
		}
}
</style> 
