<script>
	import { Blurb } from '@sveltejs/site-kit';
	import Supporters from './_components/Supporters/index.svelte';
	import Hero from './_components/Hero.svelte';
	import Image from './_components/Image.svelte';
	import Demo from './_components/Demo.svelte';
	import WhosUsingSvelte from './_components/WhosUsingSvelte/index.svelte';
	import Balls from './svelte-balls.png?w=640;1280;2560;3840&format=avif;webp;png&picture';
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

			<a href="/blog/write-less-code" class="cta">さらに詳しく</a>
		</div>

		<div slot="two">
			<h2>No virtual DOM</h2>
			<p>
				Svelteは、コードをフレームワークを含まない小さいvanilla JSにコンパイルします - アプリは高速に起動し、そのスピードを維持します
			</p>

			<a href="/blog/virtual-dom-is-pure-overhead" class="cta">さらに詳しく</a>
		</div>

		<div slot="three">
			<h2>Truly reactive</h2>
			<p>
				複雑な状態管理ライブラリは必要ありません - SvelteはJavaScriptそのものにリアクティビティをもたらします
			</p>

			<a href="/blog/svelte-3-rethinking-reactivity" class="cta">さらに詳しく</a>
		</div>

		<div class="description" slot="what">
			<p>
				Svelte(スベルト)はユーザーインタフェースを構築する先鋭的で新しいアプローチです。ReactやVueのような
				従来のフレームワークがその作業の大部分を <em>ブラウザ</em> で行うのに対し、 Svelteはその作業を
				アプリをビルドする際の <em>コンパイル時</em> に行います。
			</p>

			<p>
				Svelteは、仮想DOMによる差分検出のようなテクニックを使用する代わりに、
				アプリケーションの状態が変化したときにDOMを外科的に更新するコードを生成します。
			</p>

			<p>
				Svelteが、最近行われた3つの調査で <a
					href="https://insights.stackoverflow.com/survey/2021#section-most-loved-dreaded-and-wanted-web-frameworks"
					>最も愛されているWebフレームワーク</a
				>
				、	
				<a href="https://2020.stateofjs.com/en-US/technologies/front-end-frameworks/"
					>開発者が最も満足しているフレームワーク</a
				>
				、	
				<a
					href="https://tsh.io/state-of-frontend/#which-of-the-following-frameworks-would-you-like-to-learn-in-the-future"
					>最も学習したいフレームワーク</a
				>
				にそれぞれ選出されたことを誇りに思います。あなたにもきっと気に入って頂けると思います。もっと詳しく知りたい方は
				<a href="/blog/svelte-3-rethinking-reactivity" class="cta"
					>こちらの紹介記事</a
				> をご覧ください。
			</p>
		</div>

		<div slot="how">
			<pre><code
					>npm create svelte@latest myapp
cd myapp
npm install
npm run dev
			</code></pre>

			<a href="/tutorial" class="cta">Svelteを学ぶ</a>
		</div>
	</Blurb>
</div>

<Demo />

<section>
	<h3>Who's using Svelte?</h3>

	<WhosUsingSvelte />
</section>

<Supporters />

<Image src={Balls} alt="The Svelte logo in a ball pit" />

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
		margin: 10rem auto;
		padding: 0 var(--side-nav);
		max-width: 120rem;
	}

	.blurb-shifter {
		margin-top: calc(-10rem + var(--side-nav));
	}

	footer {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		padding: 4rem;
	}

	footer a {
		color: var(--text);
		padding: 0.5rem 1rem;
		display: block;
	}

	@media (min-width: 900px) {
		.blurb-shifter {
			margin-top: -12em;
		}
	}
</style>
