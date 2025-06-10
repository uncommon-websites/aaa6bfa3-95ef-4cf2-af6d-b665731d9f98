<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "~icons/lucide/briefcase";
	import IconUsers from "~icons/lucide/users";
	import IconHeart from "~icons/lucide/heart";
	import IconGlobe from "~icons/lucide/globe";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
  {
    title: "Remote-first, built for flexibility",
    description: "Work from anywhere in the world, around your schedule",
    icon: IconBriefcase
  },
  {
    title: "Work at NHS scale",
    description: "Help solve the UK doctor shortage and scale next-gen care",
    icon: IconUsers
  },
  {
    title: "Grow with top talent",
    description: "Founders & leaders who built $5M+ ARR startups and led at NHS scale",
    icon: IconHeart
  }
];

	const openings: JobOpening[] = [
		// Engineering
		{
			title: "Senior Frontend Developer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Backend Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Design Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Design
		{
			title: "UX/UI Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product
		{
			title: "Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Product Analyst",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Marketing
		{
			title: "Marketing Specialist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Content Strategist",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Social Media Manager",
			department: "Marketing",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
  {
    name: "Janelle Cruz",
    position: "Operations Associate",
    company: "People & Operations",
    quote:
      "From day one, I felt welcomed and valued here. My teammates and manager supported me through onboarding, and there’s always someone to help you learn and grow.",
    image:
      "/generated/image-a-filipino-woman-in-a-modern-office-sett.webp"
  },
  {
    name: "Dr. Amir Rahman",
    position: "Senior GP Contractor",
    company: "Remote Clinical Team",
    quote:
      "At Asterix Health, I can deliver patient care with real flexibility. Leadership invests in my growth, and the opportunity to impact UK healthcare from abroad is truly unique.",
    image:
      "/generated/image-a-malaysian-male-doctor-confidently-stan.webp"
  },
  {
    name: "Danielle Okoye",
    position: "Engineering Manager",
    company: "Product & Engineering",
    quote:
      "Collaboration is at the heart of everything we do. The mission inspires me, and I love having the freedom to mentor, build, and balance my life outside of work.",
    image:
      "/generated/image-a-black-british-woman-leading-a-tech-tea.webp"
  }
];

	const processSteps = [
  {
    step: 1,
    title: "Apply online",
    description:
      "Submit your CV and a short note—no long application forms."
  },
  {
    step: 2,
    title: "Meet the team",
    description:
      "Quick initial call to get to know you and align on the role."
  },
  {
    step: 3,
    title: "Task or case study",
    description:
      "A short challenge or discussion related to your work, so we can see how you think."
  },
  {
    step: 4,
    title: "Final chat with founders",
    description:
      "Last conversation with the founders for team fit and next steps."
  }
];

	const values = [
  {
    icon: IconHeart,
    title: "Move fast, with care",
    description: "We operate quickly but never lose sight of clinical trust and patient safety."
  },
  {
    icon: IconUsers,
    title: "Built on trust",
    description: "We give people real ownership and autonomy to solve hard problems responsively."
  },
  {
    icon: IconGlobe,
    title: "Global mindset",
    description: "We work across borders and time zones, and value rapid learning from different perspectives."
  }
];
</script>

<!-- Hero Section -->

<SecondaryHero
  title="Bring UK healthcare into the future"
  subtitle="Work remotely with doctors reshaping access to care"
  imageSrc="/generated/image-a-diverse-group-of-healthcare-profession.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Build your career while making an impact" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-3">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
