<script lang="ts">
	import {
		gigsSectionHeight as gs,
		musicSectionHeight as ms,
		videosSectionHeight as vs,
		gallerySectionHeight as gas,
		infoSectionHeight as is,
		contactSectionHeight as cs,
		navigationHeight as nh
	} from '$store/objectsizes.js';

	export let page = 'home';

	$: scrollY = 0;

	$: section_01 = $gs - $nh * 2;
	$: section_02 = $ms - $nh;
	$: section_03 = $vs - $nh;
	$: section_04 = $gas - $nh;
	$: section_05 = $is - $nh;
	$: section_06 = $cs - $nh;
</script>

<svelte:window bind:scrollY />

<li class="text-xl font-bold sm:text-2xl md:text-3xl xl:text-4xl 2xl:text-5xl">
	<!-- prettier-ignore -->
	<a
		href="/home/#gigs"
		class="navigation-link link 
		{page !== "legal" ? ((scrollY >= section_01 && scrollY < section_02) ? '' : 'link-hover') : "link-hover"}">Gigs
	</a>
</li>
<li class="text-xl font-bold sm:text-2xl md:text-3xl xl:text-4xl 2xl:text-5xl">
	<!-- prettier-ignore -->
	<a
		href="/home/#music"
		class="navigation-link link 
		{page !== "legal" ? ((scrollY >= section_02 && scrollY < section_03) ? '' : 'link-hover') : "link-hover"}">Musik
	</a>
</li>
<li class="text-xl font-bold sm:text-2xl md:text-3xl xl:text-4xl 2xl:text-5xl">
	<!-- prettier-ignore -->
	<a
		href="/home/#videos"
		class="navigation-link link 
		{page !== "legal" ? ((scrollY >= section_03 && scrollY < section_04) ? '' : 'link-hover') : "link-hover"}">Videos
	</a>
</li>
<li class="text-xl font-bold sm:text-2xl md:text-3xl xl:text-4xl 2xl:text-5xl">
	<!-- prettier-ignore -->
	<a
		href="/home/#gallery"
		class="navigation-link link 
		{page !== "legal" ? ((scrollY >= section_04 && scrollY < section_05) ? '' : 'link-hover') : "link-hover"}">Galerie
	</a>
</li>
<li class="text-xl font-bold sm:text-2xl md:text-3xl xl:text-4xl 2xl:text-5xl">
	<!-- prettier-ignore -->
	<a
		href="/home/#info"
		class="navigation-link link 
		{page !== "legal" ? ((scrollY >= section_05 && scrollY < section_06) ? '' : 'link-hover') : ""}">Info
	</a>
</li>
<li class="text-xl font-bold sm:text-2xl md:text-3xl xl:text-4xl 2xl:text-5xl">
	<!-- prettier-ignore -->
	<a
		href="/home/#contact"
		class="navigation-link link 
		{page !== "legal" ? ((scrollY >= section_06) ? '' : 'link-hover') : "link-hover"}">Kontakt
	</a>
</li>
