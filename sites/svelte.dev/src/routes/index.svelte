<script context="module">
	export const prerender = true;
</script>

<script>
	import { Blurb } from '@sveltejs/site-kit';
	import Supporters from './_components/Supporters/index.svelte';
	import Hero from './_components/Hero.svelte';
	import Image from './_components/Image.svelte';
	import Demo from './_components/Demo.svelte';
	import WhosUsingSvelte from './_components/WhosUsingSvelte/index.svelte';
	import Balls from '$img/svelte-balls.png?w=640;1280;2560;3840&format=avif;webp;png&meta';
</script>

<svelte:head>
	<title>Svelte • サイバネティクスで強化されたWebアプリ</title>

	<meta name="twitter:title" content="Svelte" />
	<meta name="twitter:description" content="サイバネティクスで強化されたWebアプリ" />
	<meta name="Description" content="サイバネティクスで強化されたWebアプリ" />
</svelte:head>

<h1 class="visually-hidden">Svelte</h1>

<Hero />

<div class="blurb-shifter">
	<Blurb>
		<div slot="one">
			<h2>Write less code</h2>
			<p>
				既存の言語（HTML、CSS、JavaScript）で、ボイラープレートのないコンポーネントを作成することができます
			</p>

			<a sveltekit:prefetch href="/blog/write-less-code" class="cta">さらに詳しく</a>
		</div>

		<div slot="two">
			<h2>No virtual DOM</h2>
			<p>
				Svelteは、コードをフレームワークを含まない小さいvanilla JSにコンパイルします - アプリは高速に起動し、そのスピードを維持します
			</p>

			<a sveltekit:prefetch href="/blog/virtual-dom-is-pure-overhead" class="cta">さらに詳しく</a>
		</div>

		<div slot="three">
			<h2>Truly reactive</h2>
			<p>
				複雑な状態管理ライブラリは必要ありません - SvelteはJavaScriptそのものにリアクティビティをもたらします
			</p>

			<a sveltekit:prefetch href="/blog/svelte-3-rethinking-reactivity" class="cta">さらに詳しく</a>
		</div>

		<div class="description" slot="what">
			<p>
				Svelteはユーザーインタフェースを構築する先鋭的で新しいアプローチです。ReactやVueのような
				従来のフレームワークがその作業の大部分を <em>ブラウザ</em> で行うのに対し、 Svelteはその作業を
				アプリをビルドする際の <em>コンパイル時</em> に行います。
			</p>

			<p>
				Svelteは仮想DOMによる差分検出のようなテクニックを使用する代わりに、
				アプリケーションの状態が変化したときにDOMを外科的に更新するコードを生成します。
			</p>

			<p>
				Svelteが、最近行われた2つの調査で <a
					href="https://insights.stackoverflow.com/survey/2021#section-most-loved-dreaded-and-wanted-web-frameworks"
					>最も愛されているWebフレームワーク</a
				>
				、	
				<a href="https://2020.stateofjs.com/en-US/technologies/front-end-frameworks/"
					>開発者が最も満足しているフレームワーク</a
				>
				にそれぞれ選出されたことを誇りに思います。あなたにもきっと気に入って頂けると思います。もっと詳しく知りたい方は
				<a href="/blog/svelte-3-rethinking-reactivity" class="cta"
					>こちらの紹介記事</a
				> をご覧ください。
			</p>
		</div>

		<div slot="how">
			<pre><code>
npx degit <a href="https://github.com/sveltejs/template" style="user-select: initial;"
						>sveltejs/template</a
					> my-svelte-project
cd my-svelte-project
npm install
npm run dev
			</code></pre>

			<p style="flex: 1">
				TypeScriptサポートやその他詳細については <a href="/blog/the-easiest-way-to-get-started">クイックスタートガイド</a> をご覧ください。
			</p>

			<a sveltekit:prefetch href="/tutorial" class="cta">Svelteを学ぶ</a>
		</div>
	</Blurb>
</div>

<Demo />

<section>
	<h3>Who's using Svelte?</h3>

	<WhosUsingSvelte />
</section>

<Supporters />

<Image data={Balls} alt="The Svelte logo in a ball pit" />

<footer>
	<a href="/tutorial">Tutorial</a>
	<a href="/docs">Docs</a>
	<a href="/examples">Examples</a>
	<a href="/blog">Blog</a>
	<a href="/faq">FAQ</a>
	<a href="https://opencollective.com/svelte">Open Collective</a>
</footer>

<style>
	section {
		position: relative;
		margin-inline: auto;
		margin-block: 10rem;
		padding-inline: var(--side-nav);
		max-inline-size: 120rem;
	}

	.blurb-shifter {
		margin-block-start: calc(-10rem + var(--side-nav));
	}

	footer {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		padding: 4rem;
	}

	footer a {
		color: var(--text);
		padding-inline: 1rem;
		padding-block: 0.5rem;
		display: block;
	}

	@media (min-width: 900px) {
		.blurb-shifter {
			margin-block-start: -12em;
		}
	}
</style>
