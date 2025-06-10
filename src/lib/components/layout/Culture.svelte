<script lang="ts">
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import { animate, stagger } from "motion";
	import { onMount } from "svelte";

	// Types
	export type Value = {
		title: string;
		description: string;
	};

	// Props
	const { values = [] }: { values: Value[] } = $props();

	let cards: HTMLElement[] = $state([]);

	onMount(() => {
		if (!cards.length) return;
		if (window.self !== window.top) return;

		animate(
			cards,
			{
				y: ["1.5rem", 0],
				filter: ["blur(2px)", "blur(0px)"],
				opacity: [0, 1]
			},
			{
				duration: 0.3,
				ease: "easeOut",
				delay: stagger(0.1, {
					ease: "easeInOut"
				})
			}
		);
	});
</script>

<section class="bg-white dark:bg-gray-950">
	<div
		class="section-py section-px container mx-auto grid gap-8 [--gap:--spacing(8)] [--radius:var(--radius-2xl)]"
	>
		<SectionHeader title="Built by doctors, backed by bold thinking" subtitle="The culture that drives Asterix Health" />

<div class="mb-8 text-body">
  At Asterix Health, we’re rethinking how care gets delivered—starting with who delivers it, and how. Rooted in clinical excellence and supported by proven infrastructure, we’re building a system that works for clinicians and patients alike.
</div>
<div class="mb-8 text-body">
  We believe great doctors exist beyond borders. We're here to make it easier, safer, and more cost-effective to bring their expertise into the workflows that need it most. That mission guides everything we do—from the technology choices we make to the policies we write and the way we work with our teams.
</div>

<div class="mb-8 text-title2">What we stand for</div>
<div class="grid gap-(--gap)"
  style:grid-template-columns="repeat(auto-fit, minmax(280px, 1fr))"
>
  <div bind:this={cards[0]} class="relative border-t border-gray-200 pt-4 dark:border-gray-900">
    <div class="text-caption z-10">
      <div>
        <div class="text-headline mb-[1em]">Global talent, local care</div>
        <div class="text-body text-gray-500 dark:text-gray-400">
          Exceptional care isn’t confined by geography. We connect UK-licensed doctors working remotely with the patients and practices that need them most—safely, efficiently, and at long-term scale.
        </div>
      </div>
    </div>
  </div>
  <div bind:this={cards[1]} class="relative border-t border-gray-200 pt-4 dark:border-gray-900">
    <div class="text-caption z-10">
      <div>
        <div class="text-headline mb-[1em]">Contractor-first by design</div>
        <div class="text-body text-gray-500 dark:text-gray-400">
          Every doctor working with Asterix is a contractor, giving them more flexibility and better control over their work. We provide clear clinical guidance, smooth onboarding, and consistent quality feedback without micromanagement.
        </div>
      </div>
    </div>
  </div>
  <div bind:this={cards[2]} class="relative border-t border-gray-200 pt-4 dark:border-gray-900">
    <div class="text-caption z-10">
      <div>
        <div class="text-headline mb-[1em]">Simplicity unlocks scale</div>
        <div class="text-body text-gray-500 dark:text-gray-400">
          Simpler solutions create better outcomes. We use NHS-approved tools, light-touch integration, and no-clutter workflows so teams can spend less time on process—and more on patients.
        </div>
      </div>
    </div>
  </div>
  <div bind:this={cards[3]} class="relative border-t border-gray-200 pt-4 dark:border-gray-900">
    <div class="text-caption z-10">
      <div>
        <div class="text-headline mb-[1em]">Quality without compromise</div>
        <div class="text-body text-gray-500 dark:text-gray-400">
          Every doctor we work with meets UK clinical standards, holds active GMC registration, and completes robust onboarding. We never lower the bar—only the barriers.
        </div>
      </div>
    </div>
  </div>
  <div bind:this={cards[4]} class="relative border-t border-gray-200 pt-4 dark:border-gray-900">
    <div class="text-caption z-10">
      <div>
        <div class="text-headline mb-[1em]">Regulated. Trusted. Proven.</div>
        <div class="text-body text-gray-500 dark:text-gray-400">
          We're the first and only provider with written NHS national team approval for this model. That trust matters—to our partners, our patients, and the professionals who choose to work with us.
        </div>
      </div>
    </div>
  </div>
</div>

<div class="mt-10 text-body">
  This is healthcare with fewer borders and better outcomes. If you're a doctor ready to work differently, or a provider looking for long-term relief—you're in the right place.
</div>

<div class="mt-4">
  <a href="#contact" class="text-accent underline">Learn more about working with us</a>
</div>

	</div>
</section>
