<!-- Podcast Section -->
<section id="podcast" aria-labelledby="podcast-heading">
  <!-- 1) Introducción textual -->
  <h2 id="podcast-heading">Podcast</h2>
  <p>
    At THESHAKHESTUDIUM, we don’t offer answers; we crack things open. Our podcast is a space for <strong>integral transformation</strong> with a <strong>systematic and analytical approach</strong>. In each episode:
  </p>
  <ul>
    <li>We challenge <strong>inherited beliefs</strong>, <strong>institutional taboos</strong>, and <strong>official narratives</strong>.</li>
    <li>We facilitate the <strong>collaborative discovery of hidden realities</strong> through participatory processes and constructive dialogue.</li>
    <li>We invite experts, creators, and listeners to join conversations driven by honesty, truthfulness, and empathy.</li>
  </ul>
  <p>🎧 <strong>Listen now</strong> and join the co-creation of knowledge:</p>

  <!-- 2) Spotify Player with fallback link -->
  <div class="podcast-player" role="region" aria-label="Spotify Podcast Player">
    <iframe
      src="https://open.spotify.com/embed-podcast/show/XXXXXXXXX"
      width="100%"
      height="232"
      frameborder="0"
      allow="encrypted-media"
      title="Spotify Podcast Player"
      loading="lazy">
    </iframe>
    <p>
      Can't see the player? 
      <a href="https://open.spotify.com/show/XXXXXXXXX" target="_blank" rel="noopener noreferrer">
        Listen on Spotify
      </a>.
    </p>
  </div>

  <!-- 3) Episode list -->
  <ul class="episodes" role="list">
    {% for ep in site.data.episodes %}
      <li class="episode-item" role="listitem">
        <a
          href="{{ ep.url }}"
          class="episode-link"
          aria-label="Listen to {{ ep.title }} published on {{ ep.date | date: '%B %d, %Y' }}">
          <picture>
            <source srcset="{{ ep.thumb | replace: '.jpg', '.webp' }}" type="image/webp">
            <img
              src="{{ ep.thumb }}"
              alt="Cover art for episode: {{ ep.title }}"
              loading="lazy"
              class="episode-thumbnail">
          </picture>
          <div class="episode-details">
            <h3 class="episode-title">{{ ep.title }}</h3>
            <time datetime="{{ ep.date }}">{{ ep.date | date: "%B %d, %Y" }}</time>
          </div>
        </a>
      </li>
    {% endfor %}
  </ul>

  <!-- 4) External platform buttons -->
  <nav class="podcast-links" aria-label="Other Podcast Platforms">
    <a
      href="https://podcasts.apple.com/…"
      class="btn btn-secondary"
      target="_blank"
      rel="noopener noreferrer"
      aria-label="Listen on Apple Podcasts">
      Apple Podcasts
    </a>
    <a
      href="https://www.youtube.com/playlist?list=…"
      class="btn btn-secondary"
      target="_blank"
      rel="noopener noreferrer"
      aria-label="Watch on YouTube">
      YouTube
    </a>
  </nav>
</section>

<!-- JSON-LD Structured Data -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "PodcastSeries",
  "name": "The Shakhestudium",
  "url": "https://yourdomain.com/podcast",
  "description": "A philosophical-spiritual podcast challenging conventional narratives.",
  "publisher": {
    "@type": "Organization",
    "name": "Shakhestudium LLC"
  },
  "podcastFormat": "Episodic",
  "episode": [
    {% for ep in site.data.episodes %}
    {
      "@type": "PodcastEpisode",
      "name": "{{ ep.title }}",
      "url": "https://yourdomain.com{{ ep.url }}",
      "datePublished": "{{ ep.date | date: "%Y-%m-%d" }}",
      "description": "{{ ep.description | escape }}"
    }{% unless forloop.last %},{% endunless %}
    {% endfor %}
  ]
}
</script>
