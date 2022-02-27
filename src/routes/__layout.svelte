<nav>
	<ul>
		<li>
			<a href="/">Home</a>
		</li>
		<li>
			<a href="/profile">Profile</a>
		</li>
		<li>
			<a href="/login">Login</a>
		</li>
		<li>
			<a href="/">Logout</a>
		</li>
	</ul>
</nav>

<slot />

<style>
	ul {
		display: flex;
		margin: 0;
		padding: 0;
		list-style: none;
	}
	li {
		margin-right: 20px;
		font-weight: bold;
	}
	a {
		color: #555;
		text-decoration: none;
	}
	a:hover {
		color: green;
	}
</style>
