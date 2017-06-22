# GPT Ad Polymer Element: <gpt-ad>
Web Component wrapper for Google Publisher Tags library code using Polymer.

# Usage

1. Load the GPT library at the header of your root page:

```html
<script async="async" src="https://www.googletagservices.com/tag/js/gpt.js"></script>
<script>
    var googletag = googletag || {};
    googletag.cmd = googletag.cmd || [];
</script>
```

2. Define the slots:

```html
<script>
googletag.cmd.push(function() {
    googletag.defineSlot("ad_unit_path", [300, 250], "ad_slot_example").addService(googletag.pubads());
    googletag.enableServices();
});
</script>
```

3. Import and use the gpt-ad element inside any Web Component:

```html
<link rel="import" href="gpt-ad.html">
```
```html
<gpt-ad ad-slot-id="ad_slot_example"></gpt-ad>
```