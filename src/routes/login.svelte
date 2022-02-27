<script>
	import { auth, googleProvider } from '../firebase';
	import { signInWithPopup } from 'firebase/auth';
	import { user, isLoggedIn } from '../stores';

	const login = async () => {
		try {
			const res = await signInWithPopup(auth, googleProvider);
			$user = res.user;
			$isLoggedIn = true;
		} catch (err) {
			console.error(err);
		}
	};
</script>

<h1>Login</h1>
<button on:click={login}>Login using Google</button>
