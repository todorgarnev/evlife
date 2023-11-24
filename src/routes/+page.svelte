<script lang="ts">
	import EvMasters from "$lib/components/EvMasters.svelte";
	import EvNews from "$lib/components/EvNews.svelte";
	import FindUs from "$lib/components/FindUs.svelte";
	import Footer from "$lib/components/Footer.svelte";
	import Header from "$lib/components/Header.svelte";
	import Reviews from "$lib/components/Reviews.svelte";
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
<EvNews />
<Reviews />
<EvMasters />
<FindUs />
<Footer />
