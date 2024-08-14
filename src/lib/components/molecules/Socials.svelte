<script>
	import TelegramIcon from '$lib/icons/socials/telegram.svelte';
	import InstagramIcon from '$lib/icons/socials/instagram.svelte';
</script>

<div class="socials">
	<a href="#" target="_blank" rel="noopener noreferrer" title="Say Hi on Telegram">
		<TelegramIcon />
	</a>
	<a
		href="https://instagram.com/filmbegoo_com"
		target="_blank"
		rel="noopener noreferrer"
		title="Say Hi on Telegram"
	>
		<InstagramIcon />
	</a>
</div>

<style lang="scss">
	@import '../../scss/breakpoints.scss';
	.socials {
		display: flex;
		align-items: center;
		gap: 20px;

		a {
			transition: all 0.2s ease-in-out;
			width: 24px;
			color: var(--color--text);
			fill: var(--color--text);

			&:hover {
				color: var(--color--primary);
				fill: var(--color--primary);
				filter: drop-shadow(0px 0px 3px var(--color--primary));
			}
		}
	}
</style>
