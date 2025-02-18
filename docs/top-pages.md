---
title: Top Pages
--- 

import useBaseUrl from '@docusaurus/useBaseUrl';

Your "**Top Pages**" report shows which pages your visitors are visiting the most often. You can use it to identify the most popular content on your site. Click on any page to segment your audience by those who visited that particular page. You can also click on the "**Details**" button to see the full list of pages with additional metrics. The number of pageviews, bounce rate, and time on page for the individual pages are included too.

You can also see the traffic flow by looking at the "**Entry Pages**" and "**Exit Pages**" reports. You can click on the "**Details**" button to see the full list with additional details. For entry pages details include visit duration for visits that started on a specific page and for exit pages details include the exit rate percentage.

<img alt="Top Pages" src={useBaseUrl('img/top-pages.png')} />

## Searching for pages

You can search for pages using the "**Filter**" button on the top of your dashboard.

## Grouping pages

Do you want to group all your blog posts and analyze the traffic to the blog separately from the rest of your site? The "**Page**" menu within the filter button includes option for "**contains**". Put any specific keyword to group all of your pages that contain that keyword. The "**Filter**" button also allows you to segment the dashboard by grouping multiple unrelated pages at the same time.

<img alt="Top Pages - multiple filters" src={useBaseUrl('img/top-pages-filtering-multiple-filters.png')} />

You can also group different pages or dynamic URLs by using asterisks. Track all the blog posts by using `/blog*` (if your blog subdirectory is named `blog`) or track Woocommerce checkout pages for your ecommerce (`/checkout/order-received/*`). You can add asterisks in front and back in the same way that you would use "contain" (`*keyword*`). It finds any URL containing a specific keyword.

:::note
Do you prefer to display your page groupings permanently in your dashboard? You can do so using [our pageview goals](pageview-goals.md).
:::

## Filtering out pages

Do you want to filter out traffic that has visited a specific section of your site such as your logged in pages or your order confirmation page? You can filter out pages by using the "**Filter**" button on the top of your dashboard. The "**Page**" menu within the filter button includes option for "**is not**".

### How it works

Plausible Analytics records the URL path of each page view as the visitors are browsing your site. 

* Query parameters are discarded from the path to make sure they don't show up as different pages in Plausible. This means that pages like `yoursite.com/index.php?article=some_article&page=11` will be reported as `yoursite.com/index.php` in your Plausible dashboard. If you still want some pages to be reported with the complete URL that includes the query part, [here's what you should do](custom-query-params.md)

* In some cases, you might want to provide Plausible with a custom URL to use instead of the actual URL of a page. This is especially helpful to redact and aggregate multiple pages whose URLs contain user identifiers. This is helpful both from the privacy and analytics perspective. Here's [how you can aggregate page URLs](custom-locations.md)

* Do you see identical page paths with and without a trailing slash (`/some_article` and `/some_article/`) in your pages report? This points to a duplicate content issue on the site and can be solved [with a 301 redirect](https://ahrefs.com/blog/trailing-slash/)

* If your website is a single-page application with `pushState` routing, Plausible Analytics will track page views automatically with no extra work. If you're using a frontend framework that uses the URL hash for routing, we also have a special [hash-based script](hash-based-routing.md)
