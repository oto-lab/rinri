<script setup lang="ts">
const SEARCH_URL =
  'https://www.google.com/search?q=%E6%8A%80%E8%A1%93%E8%80%85%E5%80%AB%E7%90%86'
const DISCORD_URL = 'https://discord.gg/evex'
const GITHUB_URL = 'https://github.com/EdamAme-x/rinri'

const SHARE_TEXT = '技術者倫理を守ろう。'
const SHARE_URL = 'https://技術者倫理.com'
const SHARE_HASHTAGS = '技術者倫理'

const X_SHARE_URL =
  'https://twitter.com/intent/tweet' +
  `?text=${encodeURIComponent(SHARE_TEXT)}` +
  `&url=${encodeURIComponent(SHARE_URL)}` +
  `&hashtags=${encodeURIComponent(SHARE_HASHTAGS)}`
</script>

<template>
  <main class="page">
    <section class="hero">
      <h1 class="title">技術者倫理を守ろう</h1>
      <p class="lead">エンジニアとしての誠実さを、今日も。</p>

      <div class="actions">
        <a class="cta" :href="SEARCH_URL" target="_blank" rel="noopener noreferrer">
          技術者倫理について調べる
          <span aria-hidden="true">→</span>
        </a>

        <a
          class="share"
          :href="X_SHARE_URL"
          target="_blank"
          rel="noopener noreferrer"
          aria-label="Xで共有する"
        >
          <svg
            class="x-icon"
            viewBox="0 0 24 24"
            width="18"
            height="18"
            aria-hidden="true"
          >
            <path
              fill="currentColor"
              d="M18.244 2H21.5l-7.5 8.57L23 22h-6.844l-5.36-6.99L4.6 22H1.34l8.02-9.166L1 2h7.02l4.83 6.39L18.244 2Zm-1.2 18h1.86L7.04 4H5.07L17.044 20Z"
            />
          </svg>
          <span>Xで広めよう</span>
        </a>
      </div>
    </section>

    <footer class="footer">
      <a class="link" :href="DISCORD_URL" target="_blank" rel="noopener noreferrer">
        discord.gg/evex
      </a>
      <span class="sep" aria-hidden="true">·</span>
      <a class="link" :href="GITHUB_URL" target="_blank" rel="noopener noreferrer">
        github.com/EdamAme-x/rinri
      </a>
    </footer>
  </main>
</template>

<style scoped>
.page {
  min-height: 100dvh;
  display: grid;
  grid-template-rows: 1fr auto;
  padding: 2rem 1.25rem;
  gap: 2rem;
}

.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  gap: 1.25rem;
}

.title {
  margin: 0;
  font-size: clamp(2rem, 6vw, 4rem);
  font-weight: 800;
  letter-spacing: 0.02em;
  background: linear-gradient(135deg, #38bdf8, #818cf8 55%, #f472b6);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.lead {
  margin: 0;
  color: var(--muted);
  font-size: clamp(0.95rem, 2.5vw, 1.125rem);
}

.cta {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  margin-top: 0.5rem;
  padding: 0.85rem 1.5rem;
  border-radius: 999px;
  font-weight: 600;
  font-size: 1rem;
  text-decoration: none;
  color: #0b1220;
  background: linear-gradient(135deg, #7dd3fc, #a5b4fc 55%, #f9a8d4);
  box-shadow:
    0 1px 0 rgba(255, 255, 255, 0.5) inset,
    0 10px 30px -10px rgba(129, 140, 248, 0.6);
  transition: transform 150ms ease, box-shadow 150ms ease, filter 150ms ease;
}

.cta:hover {
  transform: translateY(-1px);
  filter: brightness(1.05);
  box-shadow:
    0 1px 0 rgba(255, 255, 255, 0.6) inset,
    0 14px 36px -10px rgba(129, 140, 248, 0.75);
}

.cta:active {
  transform: translateY(0);
}

.actions {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  gap: 0.75rem;
  margin-top: 0.5rem;
}

.share {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.78rem 1.25rem;
  border-radius: 999px;
  font-weight: 600;
  font-size: 0.95rem;
  text-decoration: none;
  color: #ffffff;
  background: #000000;
  border: 1px solid rgba(255, 255, 255, 0.12);
  transition: transform 150ms ease, background 150ms ease, border-color 150ms ease;
}

.share:hover {
  transform: translateY(-1px);
  background: #1a1a1a;
  border-color: rgba(255, 255, 255, 0.25);
}

.share:active {
  transform: translateY(0);
}

@media (prefers-color-scheme: light) {
  .share {
    border-color: rgba(0, 0, 0, 0.1);
  }
}

.x-icon {
  display: block;
  flex-shrink: 0;
}

.footer {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.75rem;
  flex-wrap: wrap;
  padding-top: 1rem;
  color: var(--muted);
  font-size: 0.95rem;
}

.link {
  color: inherit;
  text-decoration: none;
  border-bottom: 1px dashed currentColor;
  padding-bottom: 1px;
  transition: color 150ms ease, border-color 150ms ease;
}

.link:hover {
  color: var(--fg);
  border-bottom-color: currentColor;
}

.sep {
  opacity: 0.5;
}
</style>
