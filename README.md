[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/googleads/gpt-ad)

# GPT Ad Polymer Element
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
<link rel="import" href="<path-to-component-folder>/gpt-ad.html">
```
```html
<gpt-ad ad-slot-id="ad_slot_example"></gpt-ad>
```

# Known Limitations

In Single-page Apps (SPA), which reuse components between page visits (including gpt-ad), the corresponding ad slots won't be refreshed.

## License

Copyright 2017 Google, Inc.

Licensed under the [Apache License, Version 2.0](LICENSE) (the "License");
you may not use this file except in compliance with the License. You may
obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
