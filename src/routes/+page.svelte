<script lang="ts">
	import Header from "$lib/components/Header.svelte";
	import ShareWithUs from "$lib/components/ShareWithUs.svelte";
	import TopBar from "$lib/components/TopBar.svelte";
	import TopNews from "$lib/components/TopNews.svelte";
	import TopTen from "$lib/components/TopTen.svelte";
</script>

<svelte:head>
	<title>EVLife</title>
</svelte:head>

<TopBar />
<Header />
<TopNews />
<ShareWithUs />
<TopTen />