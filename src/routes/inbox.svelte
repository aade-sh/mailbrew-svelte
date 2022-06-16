<script>
	import Button from '../components/button.svelte';
</script>

<section class="toolbar">
	<Button imageSource="/images/mail.svg" text="Manage" imageAlt="mail icon" type="pill" />
	<div class="spacer" />
	<Button imageSource="/images/information-circle.svg" imageAlt="help icon" type="circle" />
	<div class="spacer" />
	<Button imageSource="/images/archive.svg" imageAlt="archive icon" type="circle" />
	<div class="spacer" />
	<Button imageSource="/images/search.svg" imageAlt="search icon" type="circle" />
</section>

<style>
	section {
		display: flex;
		padding: 0.5rem 1rem;
		position: relative;
	}

	section > .spacer {
		width: 1rem;
	}
</style>
