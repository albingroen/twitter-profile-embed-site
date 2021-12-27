<script>
  const IMAGE =
    "https://res.cloudinary.com/albin-groen/image/upload/f_auto,q_auto/v1640634238/twitter-profile-embed-meta_a0gsc5.png";
  const DESCRIPTION = "Embed your Twitter profile on your website";
  const URL = "https://twitter-profile-embed.com";
  const TITLE = "Twitter Profile Embed";
</script>

<svelte:head>
  <!-- Primary Meta Tags -->
  <title>{TITLE}</title>
  <meta name="title" content={TITLE} />
  <meta name="description" content={DESCRIPTION} />

  <!-- Open Graph / Facebook -->
  <meta property="og:type" content="website" />
  <meta property="og:url" content={URL} />
  <meta property="og:title" content={TITLE} />
  <meta property="og:description" content={DESCRIPTION} />
  <meta property="og:image" content={IMAGE} />

  <!-- Twitter -->
  <meta property="twitter:card" content="summary_large_image" />
  <meta property="twitter:url" content={URL} />
  <meta property="twitter:title" content={TITLE} />
  <meta property="twitter:description" content={DESCRIPTION} />
  <meta property="twitter:image" content={IMAGE} />
</svelte:head>
