<script lang="ts">
	// Components
	import UseCases from "$lib/components/layout/UseCases.svelte";
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CustomerCardHero from "$lib/components/layout/hero-sections/CustomerCardHero.svelte";
</script>

<CustomerCardHero
  centered={false}
  title="Instant access to trusted doctors, anywhere"
  subtitle="Asterix Health connects UK healthcare providers with remote, highly qualified doctors—quickly, flexibly, and with seamless integration into clinical workflows."
  customers={[
    {
      name: "Dr. Samantha Reed",
      position: "GP partner, St Mary's NHS Trust",
      imageSrc: "/generated/image-a-white-female-healthcare-administrator-.webp",
      quote: "Reliable support that fits straight into our team’s workflow."
    },
    {
      name: "James Osei",
      position: "Head of operations, West Midlands Primary Care Group",
      imageSrc: "/generated/image-a-black-british-male-head-of-operations-.webp",
      quote: "Flexible clinical support that actually saves us time and money."
    },
    {
      name: "Amir Rahman",
      position: "NHS service manager, North Kent ICS",
      imageSrc: "/generated/image-a-south-asian-female-nhs-service-manager.webp",
      quote: "The doctors are excellent. Setup was fast and smooth."
    },
    {
      name: "Helen Morris",
      position: "Clinical lead, Careflow Health",
      imageSrc: "/generated/image-a-white-female-healthcare-administrator-.webp",
      quote: "Smart solution to a real workforce problem. Our clinicians love it."
    },
    {
      name: "Raj Patel",
      position: "Medical director, South London Health Trust",
      imageSrc: "/generated/image-an-east-asian-male-medical-director-in-a.webp",
      quote: "Finally—trusted, qualified doctors available when we need them."
    }
  ]}
/>
<LogoScroller
	label="Trusted by industry leaders"
	logoUrls={[
		"https://logo.clearbit.com/circlehealthgroup.co.uk",
		"https://logo.clearbit.com/bupa.co.uk",
		"https://logo.clearbit.com/spirehealthcare.com"
	]}
/>

<Summary
	title="Solving the healthcare staffing crisis"
	text="Asterix Health connects UK healthcare providers with remote, highly qualified doctors at a fraction of the usual cost. Instantly scale your team, streamline workflows, and deliver better care—without the wait."
/>

<Testimonials
	testimonials={[
		{
			name: "Eloise Parry",
			position: "Service Manager",
			company: "Brightwell NHS Trust",
			quote:
				"Asterix Health cut the time we spent on document review by over 60%. What used to take days now happens in hours—so our clinical team gets back to patient care sooner.",
			image: "/generated/image-a-female-nhs-service-manager-in-her-40s-.webp"
		},
		{
			name: "Musa Adeyemi",
			position: "Director of Operations",
			company: "Unity Primary Group",
			quote:
				"Integrating remote doctors from Asterix was seamless—and every compliance risk was handled up front. It’s made a huge difference in our service reliability.",
			image: "/generated/image-a-black-male-operations-director-in-his-.webp"
		},
		{
			name: "Rowena Miles",
			position: "Clinical Lead",
			company: "Wellington Health Partners",
			quote:
				"We’ve saved more than £50,000 in three months after switching to Asterix. The quality’s high—and we finally have flexibility, even at scale.",
			image: "/generated/image-a-middle-aged-white-female-clinical-lead.webp"
		}
	]}
/>

<Features
	title="Why choose Asterix Health?"
	subtitle="Six reasons providers are making the switch"
	features={[
  {
    title: "NHS-approved clinical workforce",
    description: "The only remote doctor provider granted written route approval from the NHS. Compliance and safety as standard."
  },
  {
    title: "Significant cost savings",
    description: "Reduce your staffing costs by up to 60% immediately, with the potential for 90% reduction as you scale."
  },
  {
    title: "High-quality, UK-registered doctors",
    description: "Every doctor is fully UK registered, postgraduate trained, and vetted for experience and clinical standards."
  },
  {
    title: "Flexible, seamless integration",
    description: "Doctors can join part time or full time, plugging directly into your workflows and approved NHS systems—no learning curve."
  },
  {
    title: "Fast setup & pilot launches",
    description: "Go live in days, not months. First pilots launch April; £12m ARR pipeline and rapid results proven."
  },
  {
    title: "Comprehensive clinical support",
    description: "From triage and admin to live consultations and clinical coding, our doctors handle essential NHS tasks remotely."
  }
]}
/>

<UseCases
  title="Use Cases"
  subtitle="Real-world applications for your business needs"
  useCases={[
    {
      title: "Free your team from admin overload",
      description:
        "Strained GP teams are buried in clinical documents and admin. Let our doctors handle blood test results, document reviews, and medication coding remotely—seamlessly plugging into your workflow.",
      image: "/generated/image-a-group-of-remote-doctors-in-a-cozy-home.webp",
      link: {
        href: "/use-cases/admin-relief",
        label: "Learn more"
      }
    },
    {
      title: "Extend care beyond 9–5",
      description:
        "Practices struggle to offer consultations outside typical hours. Our remote doctors deliver high-quality phone and video consultations, reducing pressure without adding headcount.",
      image: "/generated/image-a-healthcare-team-engaged-in-a-video-cal.webp",
      link: {
        href: "/use-cases/flexible-support",
        label: "Learn more"
      }
    },
    {
      title: "Keep patients off the waitlist radar",
      description:
        "Patients wait weeks or months for specialist care—turning manageable issues into crises. Asterix doctors offer proactive support while patients wait, helping reduce risk and improve outcomes.",
      image: "/generated/image-a-group-of-healthcare-staff-celebrating-.webp",
      link: {
        href: "/use-cases/waitlist-support",
        label: "Learn more"
      }
    }
  ]}
/>

<AboutTeaser />
<CallToAction
  title="End your doctor staffing crisis—without blowing your budget"
  subtitle="Get instant access to fully UK-registered, remote doctors at a fraction of the cost—on NHS-approved systems."
  description="Flexible, high-quality care with up to 90% cost savings, fully integrated into your workflow. Proven, compliant, and ready to scale."
  imageSrc="/generated/image-a-cheerful-healthcare-administrator-with.webp"
  callsToAction={[
    {
      href: "/contact",
      label: "Start your pilot",
      variant: "primary"
    },
    {
      href: "/how-it-works",
      label: "How it works",
      variant: "secondary"
    }
  ]}
/>
