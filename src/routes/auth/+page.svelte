<script>
	import 'animate.css';
	import Icon from '@iconify/svelte';

	let email = '',
		password = '';
</script>

<div class="d-flex gap-2">
	<div class="auth-container">
		<div class="box">
			<h1>Hi!</h1>
			<span>Sign in to continue</span>
			<div class="auth-input">
				<input type="email" placeholder="Email" bind:value={email} />
				<input type="password" placeholder="Password" bind:value={password} />
				<div class="auth-button">
					<button class="sign-button">Sign in</button>
					<button class="forgot-button" alt="Forgot Password">
						<Icon icon="mdi:forgot-password" />
					</button>
				</div>

				<span>Don't have account yet? <a href="">Register!</a></span>
			</div>
		</div>
	</div>
	<div class="display-container">
		<h1>Display</h1>
	</div>
</div>

<style>
	.auth-container {
		text-align: center;
		padding: 2rem;
		width: 50%;
		height: 100vh;
		background-color: #27374d;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.auth-container h1 {
		font-size: 2.5rem;
		font-weight: 600;
		margin: 0;
		color: #526d82;
	}
	.auth-container span {
		font-size: 1rem;
		font-weight: 400;
		color: #526d82;
	}
	.auth-container .box {
		background-color: #dde6ed;
		padding: 2rem;
		border-radius: 10px;
		display: flex;
		flex-direction: column;
	}
	.auth-container .auth-input {
		margin-top: 1rem;
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}
	.auth-container .auth-input input {
		border: none;
		border-radius: 5px;
		padding: 0.5rem 1rem;
		font-size: 1rem;
		width: 350px;
	}
	.auth-container .auth-input .auth-button {
		display: flex;
		justify-content: space-between;
		gap: 1rem;
	}
	.auth-container .auth-input .auth-button button {
		border: none;
		border-radius: 5px;
		padding: 0.5rem 1rem;
		font-size: 1rem;
		font-weight: 600;
		color: #dde6ed;
	}
	.auth-container .auth-input .auth-button button:hover {
		opacity: 0.7;
	}
	.auth-container .auth-input .auth-button button:disabled {
		opacity: 0.2;
		background-color: #526d82;
	}
	.forgot-button {
		background-color: #ff3434;
	}
	.sign-button {
		background-color: #526d82;
		width: 100%;
	}
</style>
