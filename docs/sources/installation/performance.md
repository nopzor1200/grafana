---
page_title: Performance Tips
page_description: Grafana performance tips
page_keywords: grafana, performance, documentation
---

# Performance tips

## Graphite

Graphite 0.9.13 adds a much needed feature (maxDataPoints) to its JSON rendering API that is very important for Grafana. 

If you are experiencing slow loading times for larger time ranges and are using Graphite, make sure you are running Graphite 0.9.13 or later. Older versions do not support maxDataPoints, which can cause Graphite to returns hundreds of thousands of data points for a single panel. This is especially bad for larger time ranges with higher sampling rates, and can hang your browser.

Make sure to upgrade to [0.9.13](http://graphite.readthedocs.org/en/latest/releases/0_9_13.html).


