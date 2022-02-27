<script>
	import { auth, googleProvider } from '../firebase';
	import { signInWithPopup } from 'firebase/auth';

	const login = async () => {
		try {
			const res = await signInWithPopup(auth, googleProvider);
			console.log(res.user);
		} catch (err) {
			console.error(err);
		}
	};
</script>

<h1>Login</h1>
<button on:click={login}>Login using Google</button>
