# OC Site Performance

This page describes common issues affecting the openclimate site performance and the steps involved to resolve them.

### Why this is important
Site velocity is important for a successful user experience, SEO, rankings,  and revisits.

### Factors affecting performance

### 🏋🏻 Page weight

The the amount of resources a website needs to load makes a huge impact on site performance. These resources include:
- Large JS files
- High def images
- Heavy CSS files
- Large text files
- Dev - tools like (React Dev tools)

### 🕸️ Network conditions
Even if a site is build to be lightweight, it may not load quickly in browsers due to the slow network (beyond developers hands).

### 📍 Host Location
If content has to travel a long way to arrive where it is needed, this results in a high amount of network latency.

### How we measure site performance
We are using a built Google Chrome tool called lighthouse which tests, diagnoses and creates reports that includes performance, SEO,  best practices and accessibility. A test was done and generated the following results.
![performance.png](/assets/img/performance.png)

### Performance Metrics
1. **First Contentful Paint**: marks the time at which the first text or image is painted
2. **Speed Index**: shows how quickly the contents of a page are visibly populated
3. **Largest Contentful Paint**: marks the time at which the largest text or image is painted
4. **Time to Interactive**: the amount of time it takes for the page to become fully interactive
5. **Total Blocking Time**: Sum of all time periods between FCP and Time to Interactive, when task length exceeded 50ms, expressed in milliseconds
6. **Cumulative Layout Shift**: measures the movement of visible elements within the viewport

## Opportunities to improving these metrics

### Enable text compression

Text-based resources should be served with compression (***gzip***) to minimize total network bytes

### Reduce unused JavaScript

- Reduce unused JavaScript and defer loading scripts until they are required to decrease bytes by network activity
- If SSR is not being used split your JS bundles with ‘React.lazy()’. Otherwise, code-split using a third-party library such as loadable-components.
    - [JS bundle code-split with React.lazy()](https://web.dev/code-splitting-suspense/?utm_source=lighthouse&utm_medium=devtools)
    - [JS bundle code-split with loadable-components](https://loadable-components.com/docs/getting-started/)
- Removing unused imports or packages from JS files

### Serve images in next-gen formats

Image formats like WebP and AVIF often provide better compression than PNG and JPEG, which means faster downloads and less data consumption.

### Minify JavaScript

Minifying JS files can reduce payload sizes and script parse time
