<nav>
	<a href="/basic">Basic</a>
	<a href="/numeral">Numeral</a>
	<a href="/select">Select</a>
	<a href="/date">Date</a>
</nav>
<br />
<main>
	<slot />
</main>

<style>
	nav {
		display: flex;
		overflow: hidden;
		background-color: rgb(74, 84, 164);
		position: fixed;
		top: 0;
		width: 100%;
		z-index: 100;
	}

	nav a {
		float: left;
		color: #f2f2f2;
		text-align: center;
		padding: 14px 16px;
		text-decoration: none;
		font-size: 17px;
	}

	nav a:hover {
		background: #ddd;
		color: black;
	}

	main {
		padding: 16px;
		margin-top: 30px;
		height: 1500px; /* Used in this example to enable scrolling */
	}

	:global([role='listbox']) {
		margin: 0;
	}
</style>
