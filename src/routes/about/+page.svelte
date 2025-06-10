<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Innovation",
			description: "Constantly challenging the status quo to create better solutions."
		},
		{
			title: "Integrity",
			description: "Building trust through transparent actions and honest communication."
		},
		{
			title: "Impact",
			description: "Measuring our success by the positive change we create for our clients."
		}
	];
</script>

<SecondaryHero
	title="Remote doctors for UK healthcare"
	subtitle="Cut staffing costs by 60%. NHS-approved. Fast access to top clinical talent."
	imageSrc="/mockups/airport-screen-1749573264662.png"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"The UK is running out of doctors. Demand is growing, waitlists are getting longer, and traditional staffing models can’t keep up—too slow, too expensive, too rigid. Asterix Health was born from this crisis. Our founders, Julian Titz and Max Thilo, saw an opportunity to rethink how care is delivered by tapping into a qualified, global workforce—one that had never been possible to access due to outdated systems and regulatory bottlenecks.",
		"With new NHS routes now open, we’ve built the first compliance-approved pathway to bring in remote clinicians who are fully registered, postgrad qualified, and ready to work—wherever they live. We start with clinical admin but go much further: referrals, medication reviews, blood tests, consultations and full GP support—all delivered by doctors integrated directly into your existing systems. They’re cost-effective (saving providers up to 60%), schedule-flexible, and workflow-ready from day one.",
		"We’re just getting started. Our first pilots launch this spring, with £45k signed and over £12m in pipeline ARR. We’re forecasting £3.5m in ARR in the next year with a vision for 1,000+ doctors across UK healthcare. The goal is simple: build the easiest way for providers to access care capacity—without the cost, the wait, or the burnout."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
  stakeholderType="team"
  title="Our team."
  subtitle="Your partners in healthcare innovation."
  stakeholders={[
    {
      name: "Julian Titz",
      position: "Co-founder & CEO",
      bio: "Seasoned founder. Built a consumer finance app to 50,000 users and $5M ARR. Founded a next-gen telco and led global regulatory strategy.",
      image: "/generated/image-a-headshot-portrait-of-a-european-male-f.webp"
    },
    {
      name: "Max Thilo",
      position: "Co-founder & COO",
      bio: "Ex-health and trade research for ERG at UK Parliament. Published in-depth study of Singapore's healthcare system.",
      image: "/generated/image-a-headshot-portrait-of-a-european-male-o.webp"
    },
    {
      name: "Dr. Dan Bunstone",
      position: "Chief Medical Officer",
      bio: "Ex-CMO at PushDoctor. 15+ year GP partner. Co-founder at DICE.",
      image: "/generated/image-a-headshot-portrait-of-a-caucasian-male-.webp"
    },
    {
      name: "Lauren Yates",
      position: "Head of Quality",
      bio: "Ex-head of quality at PushDoctor. Governance expert. Led new vertical at BT Health.",
      image: "/generated/image-a-headshot-portrait-of-a-caucasian-femal.webp"
    }
  ]}
/>





<!-- CTA Section -->
<CallToAction
	title="Ready to collaborate?"
	subtitle="Let's create something amazing"
	description="Join the companies already leveraging our expertise to transform their digital presence and achieve their business goals."
/>
