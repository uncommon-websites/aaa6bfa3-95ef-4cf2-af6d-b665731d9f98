<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
  testimonials={[
    {
      name: "Dr. Amira Chowdhury",
      position: "Operations Lead",
      company: "Shropshire NHS Trust",
      quote:
        "We reduced admin costs by more than half without sacrificing care. Asterix Health made it easy to stay compliant and support our overstretched team, right from day one.",
      image: "/generated/image-a-british-indian-female-healthcare-opera.webp"
    },
    {
      name: "Felix Adu",
      position: "Chief Medical Officer",
      company: "Thrivemed Clinics",
      quote:
        "Bringing in Asterix Health gave us access to experienced doctors and 60% cost savings compared to usual agencies. Our ROI has been crystal clear from the first month.",
      image: "/generated/image-a-black-british-male-cmo-is-depicted-in-.webp"
    },
    {
      name: "Dr. Adila Leong",
      position: "Practice Manager",
      company: "Sungai GP Partners",
      quote:
        "The transition was so smooth—even for our older team members. Integration took less than a week and now we finally have time for patient care again.",
      image: "/generated/image-a-malaysian-female-gp-practice-manager-i.webp"
    }
  ]}
/>

<CallToAction
  title="The doctor shortage isn’t going away. We found a new supply."
  subtitle="Asterix Health gives UK healthcare providers instant access to highly qualified doctors—remotely, flexibly, and at 60% lower cost."
  description="Approved by the NHS, Asterix Health powers a new model of care—helping you cut costs, fill clinical gaps, and scale your team with top-quality remote doctors. Get started in days, not months. Simple onboarding. Proven results."
  imageSrc="/generated/image-a-cheerful-healthcare-worker-in-a-bright.webp"
  callsToAction={[
    { href: '/contact', label: 'Get access to remote doctors now', variant: 'primary' },
    { href: '/get-started', label: 'Start your pilot', variant: 'secondary' }
  ]}
/>
