<script>
	import { Button, Card, Badge, Timeline, TimelineItem, Heading, P } from 'flowbite-svelte';
	import { 
		ArrowRight, 
		Shield, 
		Users, 
		Coins, 
		Settings, 
		Globe, 
		Lock, 
		Zap,
		Database,
		Code,
		Network,
		CheckCircle
	} from 'lucide-svelte';

	const features = [
		{
			icon: Shield,
			title: 'Digital Governance',
			description: 'Implement transparent, automated governance systems with the Generalized Global Governance (GGG) standard.',
			color: 'blue'
		},
		{
			icon: Coins,
			title: 'Financial Management',
			description: 'Comprehensive treasury management with ckBTC integration, secure transfers, and trading capabilities.',
			color: 'green'
		},
		{
			icon: Settings,
			title: 'Modular Extensions',
			description: 'Sophisticated extension system allowing custom functionality to be packaged and deployed seamlessly.',
			color: 'purple'
		},
		{
			icon: Users,
			title: 'Citizen Dashboard',
			description: 'Intuitive interface for citizens to participate in governance, access services, and manage their digital identity.',
			color: 'orange'
		},
		{
			icon: Lock,
			title: 'Decentralized Auth',
			description: 'Secure, passwordless authentication using Internet Identity for enhanced privacy and security.',
			color: 'red'
		},
		{
			icon: Globe,
			title: 'Internet Computer',
			description: 'Built on the Internet Computer for true decentralization, scalability, and censorship resistance.',
			color: 'cyan'
		}
	];

	const gggEntities = [
		{ name: 'Realm', description: 'Top-level governance domain with associated treasury' },
		{ name: 'Mandate', description: 'Governance policies and regulations' },
		{ name: 'Task', description: 'Scheduled work units with automated execution' },
		{ name: 'Trade', description: 'Bilateral asset exchanges between parties' },
		{ name: 'Transfer', description: 'Asset movements with full audit trail' },
		{ name: 'Treasury', description: 'Financial vault linked to governance realm' }
	];

	const extensions = [
		{
			name: 'Vault Manager',
			description: 'ckBTC financial management and treasury operations',
			features: ['Balance tracking', 'Secure transfers', 'Transaction history', 'Multi-account support']
		},
		{
			name: 'Citizen Dashboard',
			description: 'Governance participation interface for members',
			features: ['Public services access', 'Tax information', 'Personal data management', 'Voting interface']
		},
		{
			name: 'Test Bench',
			description: 'Development and testing tools for extensions',
			features: ['Extension testing', 'API debugging', 'Performance monitoring', 'Development utilities']
		}
	];
</script>

<svelte:head>
	<title>Realms GOS - Governance Operating System</title>
	<meta name="description" content="Progressive digital sovereign realm pioneering governance of digital assets, identity, and social contracts. Built on the Internet Computer with the Generalized Global Governance standard." />
</svelte:head>

<!-- Hero Section -->
<section class="hero-gradient text-white">
	<div class="mx-auto max-w-screen-xl px-4 py-32 lg:flex lg:h-screen lg:items-center">
		<div class="mx-auto max-w-4xl text-center">
			<Heading tag="h1" class="mb-6 text-4xl font-extrabold tracking-tight text-white sm:text-6xl">
				Realms GOS
			</Heading>
			<Heading tag="h2" class="mb-8 text-xl font-light text-blue-100 sm:text-2xl">
				Governance Operating System
			</Heading>
			<P class="mb-8 text-lg text-blue-100 sm:text-xl max-w-3xl mx-auto">
				A progressive digital sovereign realm pioneering governance of digital assets, identity, and social contracts. 
				Built on the Internet Computer with the Generalized Global Governance (GGG) standard.
			</P>
			<div class="flex flex-col gap-4 sm:flex-row sm:justify-center">
				<Button size="xl" class="bg-white text-blue-600 hover:bg-blue-50">
					Explore Features
					<ArrowRight class="ml-2 h-5 w-5" />
				</Button>
				<Button size="xl" color="alternative" class="border-white text-white hover:bg-white/10">
					View on GitHub
				</Button>
			</div>
		</div>
	</div>
</section>

<!-- About Section -->
<section id="about" class="section-padding bg-white dark:bg-gray-900">
	<div class="mx-auto max-w-screen-xl px-4">
		<div class="mx-auto max-w-3xl text-center mb-16">
			<Heading tag="h2" class="mb-6 text-3xl font-bold text-gray-900 dark:text-white sm:text-4xl">
				What is Realms GOS?
			</Heading>
			<P class="text-lg text-gray-600 dark:text-gray-300">
				Realms GOS is a comprehensive governance operating system that implements the Generalized Global Governance (GGG) standard. 
				It provides the infrastructure for digital governance, decentralized autonomous organizations (DAOs), and transparent 
				financial management on the Internet Computer.
			</P>
		</div>

		<div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
			<Card class="text-center card-hover">
				<Database class="mx-auto mb-4 h-12 w-12 text-blue-600" />
				<Heading tag="h3" class="mb-2 text-xl font-semibold">GGG Standard</Heading>
				<P class="text-gray-600 dark:text-gray-300">
					Implements the Generalized Global Governance standard with entities for mandates, tasks, licenses, and organizational structures.
				</P>
			</Card>

			<Card class="text-center card-hover">
				<Network class="mx-auto mb-4 h-12 w-12 text-green-600" />
				<Heading tag="h3" class="mb-2 text-xl font-semibold">Decentralized</Heading>
				<P class="text-gray-600 dark:text-gray-300">
					Built on the Internet Computer for true decentralization, ensuring censorship resistance and global accessibility.
				</P>
			</Card>

			<Card class="text-center card-hover">
				<Code class="mx-auto mb-4 h-12 w-12 text-purple-600" />
				<Heading tag="h3" class="mb-2 text-xl font-semibold">Extensible</Heading>
				<P class="text-gray-600 dark:text-gray-300">
					Modular architecture with a sophisticated extension system allowing custom functionality to be packaged and deployed.
				</P>
			</Card>
		</div>
	</div>
</section>

<!-- Features Section -->
<section id="features" class="section-padding bg-gray-50 dark:bg-gray-800">
	<div class="mx-auto max-w-screen-xl px-4">
		<div class="mx-auto max-w-3xl text-center mb-16">
			<Heading tag="h2" class="mb-6 text-3xl font-bold text-gray-900 dark:text-white sm:text-4xl">
				Core Features
			</Heading>
			<P class="text-lg text-gray-600 dark:text-gray-300">
				Realms GOS provides a comprehensive suite of tools for digital governance, financial management, and community participation.
			</P>
		</div>

		<div class="grid gap-8 md:grid-cols-2 lg:grid-cols-3">
			{#each features as feature}
				<Card class="card-hover">
					<div class="flex items-center mb-4">
						<div class="rounded-lg bg-{feature.color}-100 p-3 dark:bg-{feature.color}-900">
							<svelte:component this={feature.icon} class="h-6 w-6 text-{feature.color}-600 dark:text-{feature.color}-400" />
						</div>
						<Heading tag="h3" class="ml-4 text-xl font-semibold">{feature.title}</Heading>
					</div>
					<P class="text-gray-600 dark:text-gray-300">{feature.description}</P>
				</Card>
			{/each}
		</div>

		<!-- GGG Entities -->
		<div class="mt-16">
			<Heading tag="h3" class="mb-8 text-2xl font-bold text-center text-gray-900 dark:text-white">
				GGG Governance Entities
			</Heading>
			<div class="grid gap-6 md:grid-cols-2 lg:grid-cols-3">
				{#each gggEntities as entity}
					<div class="rounded-lg border border-gray-200 bg-white p-6 dark:border-gray-700 dark:bg-gray-900">
						<div class="flex items-center mb-2">
							<CheckCircle class="mr-2 h-5 w-5 text-green-500" />
							<Heading tag="h4" class="text-lg font-semibold">{entity.name}</Heading>
						</div>
						<P class="text-sm text-gray-600 dark:text-gray-300">{entity.description}</P>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>

<!-- Extensions Section -->
<section class="section-padding bg-white dark:bg-gray-900">
	<div class="mx-auto max-w-screen-xl px-4">
		<div class="mx-auto max-w-3xl text-center mb-16">
			<Heading tag="h2" class="mb-6 text-3xl font-bold text-gray-900 dark:text-white sm:text-4xl">
				Extension Ecosystem
			</Heading>
			<P class="text-lg text-gray-600 dark:text-gray-300">
				Realms GOS features a powerful extension system that allows developers to create custom functionality 
				and deploy it seamlessly within the governance framework.
			</P>
		</div>

		<div class="grid gap-8 lg:grid-cols-3">
			{#each extensions as extension}
				<Card class="card-hover">
					<Heading tag="h3" class="mb-4 text-xl font-semibold">{extension.name}</Heading>
					<P class="mb-4 text-gray-600 dark:text-gray-300">{extension.description}</P>
					<div class="space-y-2">
						{#each extension.features as feature}
							<div class="flex items-center">
								<CheckCircle class="mr-2 h-4 w-4 text-green-500" />
								<span class="text-sm text-gray-600 dark:text-gray-300">{feature}</span>
							</div>
						{/each}
					</div>
				</Card>
			{/each}
		</div>
	</div>
</section>

<!-- Vision Section -->
<section id="vision" class="section-padding gradient-bg text-white">
	<div class="mx-auto max-w-screen-xl px-4">
		<div class="mx-auto max-w-4xl text-center">
			<Heading tag="h2" class="mb-8 text-3xl font-bold sm:text-4xl">
				The Future of Digital Governance
			</Heading>
			<P class="mb-8 text-lg text-blue-100">
				Realms GOS envisions a world where governance is transparent, participatory, and efficient. 
				By leveraging blockchain technology and the Internet Computer, we're building the infrastructure 
				for the next generation of digital societies.
			</P>
			
			<div class="grid gap-8 md:grid-cols-2 mt-12">
				<div class="text-left">
					<Heading tag="h3" class="mb-4 text-xl font-semibold">For Organizations</Heading>
					<ul class="space-y-2 text-blue-100">
						<li class="flex items-center">
							<CheckCircle class="mr-2 h-5 w-5" />
							Transparent decision-making processes
						</li>
						<li class="flex items-center">
							<CheckCircle class="mr-2 h-5 w-5" />
							Automated policy enforcement
						</li>
						<li class="flex items-center">
							<CheckCircle class="mr-2 h-5 w-5" />
							Secure financial management
						</li>
						<li class="flex items-center">
							<CheckCircle class="mr-2 h-5 w-5" />
							Scalable governance structures
						</li>
					</ul>
				</div>
				
				<div class="text-left">
					<Heading tag="h3" class="mb-4 text-xl font-semibold">For Citizens</Heading>
					<ul class="space-y-2 text-blue-100">
						<li class="flex items-center">
							<CheckCircle class="mr-2 h-5 w-5" />
							Direct participation in governance
						</li>
						<li class="flex items-center">
							<CheckCircle class="mr-2 h-5 w-5" />
							Secure digital identity management
						</li>
						<li class="flex items-center">
							<CheckCircle class="mr-2 h-5 w-5" />
							Access to public services
						</li>
						<li class="flex items-center">
							<CheckCircle class="mr-2 h-5 w-5" />
							Financial sovereignty
						</li>
					</ul>
				</div>
			</div>
		</div>
	</div>
</section>

<!-- Architecture Section -->
<section id="architecture" class="section-padding bg-gray-50 dark:bg-gray-800">
	<div class="mx-auto max-w-screen-xl px-4">
		<div class="mx-auto max-w-3xl text-center mb-16">
			<Heading tag="h2" class="mb-6 text-3xl font-bold text-gray-900 dark:text-white sm:text-4xl">
				Technical Architecture
			</Heading>
			<P class="text-lg text-gray-600 dark:text-gray-300">
				Built with modern technologies and best practices for scalability, security, and developer experience.
			</P>
		</div>

		<div class="grid gap-8 lg:grid-cols-2">
			<Card>
				<Heading tag="h3" class="mb-4 text-xl font-semibold">Backend Infrastructure</Heading>
				<div class="space-y-4">
					<div class="flex items-center">
						<Badge color="blue" class="mr-3">Python</Badge>
						<span>Kybra framework for Internet Computer development</span>
					</div>
					<div class="flex items-center">
						<Badge color="green" class="mr-3">Database</Badge>
						<span>kybra-simple-db for entity relationships and audit logging</span>
					</div>
					<div class="flex items-center">
						<Badge color="purple" class="mr-3">Extensions</Badge>
						<span>Dynamic loading and execution of packaged extensions</span>
					</div>
					<div class="flex items-center">
						<Badge color="orange" class="mr-3">APIs</Badge>
						<span>RESTful APIs for governance entities and operations</span>
					</div>
				</div>
			</Card>

			<Card>
				<Heading tag="h3" class="mb-4 text-xl font-semibold">Frontend Experience</Heading>
				<div class="space-y-4">
					<div class="flex items-center">
						<Badge color="red" class="mr-3">SvelteKit</Badge>
						<span>Modern web framework for reactive user interfaces</span>
					</div>
					<div class="flex items-center">
						<Badge color="cyan" class="mr-3">Tailwind</Badge>
						<span>Utility-first CSS framework for rapid UI development</span>
					</div>
					<div class="flex items-center">
						<Badge color="yellow" class="mr-3">Flowbite</Badge>
						<span>Component library for consistent design system</span>
					</div>
					<div class="flex items-center">
						<Badge color="indigo" class="mr-3">TypeScript</Badge>
						<span>Type-safe development with enhanced developer experience</span>
					</div>
				</div>
			</Card>
		</div>

		<div class="mt-12 text-center">
			<Card class="max-w-2xl mx-auto">
				<Heading tag="h3" class="mb-4 text-xl font-semibold">Internet Computer Integration</Heading>
				<P class="text-gray-600 dark:text-gray-300 mb-4">
					Realms GOS leverages the Internet Computer's unique capabilities for true decentralization, 
					including Internet Identity for authentication, ckBTC for financial operations, and 
					canister smart contracts for governance logic.
				</P>
				<div class="flex justify-center space-x-4">
					<Badge color="blue">Decentralized</Badge>
					<Badge color="green">Scalable</Badge>
					<Badge color="purple">Secure</Badge>
					<Badge color="orange">Efficient</Badge>
				</div>
			</Card>
		</div>
	</div>
</section>

<!-- CTA Section -->
<section class="section-padding bg-white dark:bg-gray-900">
	<div class="mx-auto max-w-screen-xl px-4 text-center">
		<Heading tag="h2" class="mb-6 text-3xl font-bold text-gray-900 dark:text-white sm:text-4xl">
			Ready to Build the Future?
		</Heading>
		<P class="mb-8 text-lg text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">
			Join the Realms GOS community and help shape the future of digital governance. 
			Whether you're a developer, organization, or citizen, there's a place for you in the ecosystem.
		</P>
		<div class="flex flex-col gap-4 sm:flex-row sm:justify-center">
			<Button size="xl" href="https://github.com/smart-social-contracts/realms" target="_blank">
				<Code class="mr-2 h-5 w-5" />
				Explore the Code
			</Button>
			<Button size="xl" color="alternative">
				<Users class="mr-2 h-5 w-5" />
				Join the Community
			</Button>
		</div>
	</div>
</section>
