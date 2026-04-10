<script>
	import Icon from '$lib/components/Icon.svelte';
	import { mdiEmail, mdiFacebook, mdiPhone } from '@mdi/js';
</script>

<div class="icon-line grid">
	<Icon mdi={mdiPhone} size="1" fill="--color-emerald-900" />
	<p>900 71 827</p>
</div>

<div class="icon-line grid">
	<Icon mdi={mdiEmail} size="1" fill="--color-emerald-900" />
	<a href="/" class="">Mail</a>
</div>

<div class="icon-line grid">
	<Icon mdi={mdiFacebook} size="1" fill="--color-emerald-900" />
	<a href="https://www.facebook.com/profile.php?id=61571948758888" class="">Facebook</a>
</div>
