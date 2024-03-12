---
import { SITE } from '~/config.mjs';
import { getCanonical, getHomePermalink } from '~/utils/permalinks';
import Layout from '~/layouts/PageLayout.astro';
import { Icon } from 'astro-icon';

const meta = {
	title: SITE.title,
	description: SITE.description,
	canonical: getCanonical(getHomePermalink()),
};

const items = [
	{
		title: 'Arkhadian',
		description:
			'mainnet',
		icon: 'arkhadian',
		Link: 'https://service.sychonix.me/mainnet/arkhadian',
	},
	{
		title: 'Blockx',
		description:
			'mainnet',
		icon: 'blockx',
		Link: 'https://service.sychonix.me/mainnet/blockx',
	},
{
		title: 'Decentr',
		description:
			'mainnet',
		icon: 'decentr',
		Link: 'https://service.sychonix.me/mainnet/decentr',
	},
	{
		title: 'Empower',
		description:
			'mainnet',
		icon: 'empower',
		Link: 'https://service.sychonix.me/mainnet/empower',
	},
	{
		title: 'Terp',
		description:
			'mainnet',
		icon: 'terp',
		Link: 'https://service.sychonix.me/mainnet/terp',
	},
];
---
<Layout {meta}>
<section class="scroll-mt-16" id="feature3">
	<div class="absolute inset-0 bg-primary-50 dark:bg-slate-800 pointer-events-none mb-32" aria-hidden="true"></div>
	<div class="relative max-w-6xl mx-auto px-4 sm:px-6">
		<div class="py-4 pt-8 sm:py-6 lg:py-8 lg:pt-12">
			<div class="mb-8 text-center">
				<!-- <p class="text-base text-primary-600 dark:text-primary-200 font-semibold tracking-wide uppercase">Components</p> -->
				<h2 class="text-4xl md:text-5xl font-bold leading-tighter tracking-tighter mb-4 font-heading">
					mainnet
				</h2>
				<p class="max-w-3xl mx-auto text-center text-xl text-gray-600 dark:text-slate-400">
					Sychonix Supports Mainnet and Providing Services
				</p>
			</div>
			<div class="grid gap-6 md:grid-cols-2 lg:grid-cols-3 items-center my-12 dark:text-white">
				{
					items.map(({ title, description, icon , Link }) => (
						<div class="relative flex flex-col p-6 bg-gray dark:bg-slate-900 rounded shadow-xl hover:shadow-lg transition dark:border dark:border-slate-800">
							<a href={Link}>
								<Icon name={icon} class="w-12 h-12 mx-auto my-4 cursor-pointer transition duration-200 ease-in-out transform hover:scale-150" />
							</a>
							<p class="text-black dark:text-black text-md items-center font font-semibold text-center">{title}</p>
						</div>
					))
				}
			</div>
			</div>
						</div>
</section>
</Layout>
