<script>
	import { user, isLoggedIn } from '../stores';
</script>

<h1>Profile</h1>
{#if $isLoggedIn}
	<div class="profile">
		<img width="80" height="80" src={$user.photoURL} alt="user" />
		<h4>{$user.displayName}</h4>
		<p>Your email is {$user.email}</p>
	</div>
{/if}

<style>
	.profile {
		display: grid;
		place-items: center;
		min-width: 500px;
		border: 2px solid #ddd;
		margin: 20px;
		padding: 20px;
		background-color: lightgreen;
	}
	img {
		border-radius: 100%;
	}
	h4 {
		margin: 0;
	}
</style>
