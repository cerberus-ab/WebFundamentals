project_path: /web/tools/_project.yaml
book_path: /web/tools/_book.yaml
description: TODO

{# wf_updated_on: 2019-02-01 #}
{# wf_published_on: 2019-02-01 #}
{# wf_blink_components: Platform>DevTools #}

# Get Started With Inspecting Network Activity In Chrome DevTools {: .page-title }

{% include "web/_shared/contributors/kaycebasques.html" %}

This hands-on tutorial teaches you how to use Chrome DevTools to inspect a web page's
network activity.

## When to use the Network panel {: #overview }

In general, use the Network panel when you need to make sure that resources are being
downloaded or uploaded as expected. The most common use cases for the Network panel are:

* Making sure that resources are actually being uploaded or downloaded at all.
* Inspecting the properties of an individual resource, such as its HTTP headers, content,
  size, and so on.

[speed]: /web/tools/chrome-devtools/speed/get-started

If you're looking for ways to improve page load performance, *don't* start with the Network
panel. There are many types of load performance issues that aren't related to network
activity. Start with the Audits panel because it gives you targeted suggestions on how to
improve your page. See [Optimize Website Speed][speed].

## Open the Network panel {: #open }

This is a hands-on tutorial. You're going to open up DevTools alongside web pages
in order to gain firsthand experience with the Network panel.

1. Open the [Get Started Demo](https://devtools.glitch.me/network/basics.html){: .external }.

     You might prefer to move the demo to a separate window.

1. [Open DevTools](/web/tools/chrome-devtools/open) by pressing
   <kbd>Control</kbd>+<kbd>Shift</kbd>+<kbd>J</kbd> or 
   <kbd>Command</kbd>+<kbd>Option</kbd>+<kbd>J</kbd> (Mac). The **Console**
   panel opens.
1. Click the **Network** tab. The Network panel opens.

     You might prefer to dock DevTools to the bottom of your window.

## Simulate a slower network connection {: #throttle }

The network connection of the computer that you use to build sites is probably
faster than the network connections of your users on mobile devices. By throttling the page
you can get a better idea of how long a page takes to load on a mobile device.

1. Click the **Throttling** dropdown, which is probably set to **Online**.
1. Select **Slow 3G**.

<aside class="objective">
  <b>Tip!</b> See <a href="/web/tools/chrome-devtools/device-mode/">Simulate Mobile Devices
  With Device Mode</a> to discover other DevTools features related to simulating
  mobile devices, such as overriding geolocation and simulating different device orientations.
</aside>

## Log page load activity {: #load }

Right now the Network panel is empty. That's because DevTools only logs network activity
while it's open and no network activity has occurred since you opened DevTools.

On most web pages, the great majority of network activity occurs while a page is loading.
Since DevTools only records network activity when it's open, you need to open DevTools first
and then reload a page in order to see the network activity that occurs while the page is
loading.

[reload]: /web/tools/chrome-devtools/images/shared/reload.png

1. Click **Reload** ![Reload][reload]{: .inline-icon }. The Network panel logs all network
   activity that occurs while the page is loading in the **Network Log**.
1. Sometimes you need to reproduce the page loading experience of a first-time visitor
   to your site. Try it now by long-pressing **Reload** ![Reload][reload]{: .inline-icon }
   and then selecting **Empty Cache And Hard Reload**.

## The Network Log {: #log }

Each row of the **Network Log** represents a resource. By default the resources are listed
chronologically. The network activity for the top resource initiated first, and the network
activity for the bottom resource initiated last.
When inspecting page load network activity, the top resource is usually the network request for
the main HTML document.

### Add a column to the Network Log {: #customize }

1. Right-click the header of the **Network Log**.

[priority]: /web/fundamentals/performance/resource-prioritization

1. Select **Priority**. A new **Priority** column is added to the **Network Log**.
   This column tells you what [priority][priority] the browser assigned to the resource.

## Log runtime network activity {: #runtime }

So long as you've got DevTools open, it will record network activity in the Network Log.

1. Look at the bottom of the **Network Log** and make a mental note of the last activity.
1. In the demo, click **Get Data**.
1. Look at the bottom of the **Network Log** again. There's a new resource called
   `getstarted.json`. Clicking the **Get Data** button caused the page to request
   `getstarted.json`.

## Inspect a resource's details {: #details }

## Search network headers and responses {: #search }

[policy]: /web/tools/lighthouse/audits/cache-policy

## Filter resources {: #filter }

### Filter by resource type {: #type }

Hold Command and click to select multiple.

## Test your knowledge {: #test }

Answer the questions below to reinforce the knowledge and skills that you learned throughout
this tutorial.

<div class="devsite-tracking-question">
  <div>
    When figuring out how to improve load performance, the Network panel is the best place
    to start.
  </div>
  <div class="gc-analytics-event"
       data-category="TODO" data-value="1"
       data-label="TODO">
    <div>True</div>
    <div>TODO</div>
  </div>
  <div class="gc-analytics-event"
       data-category="TODO" data-value="0"
       data-label="TODO">
    <div>False</div>
    <div>TODO</div>
  </div>
</div>

<div class="devsite-tracking-question">
  <div>
    Sometimes the Network panel is empty. Why is that?
  </div>
  <div class="gc-analytics-event"
       data-category="TODO" data-value="1"
       data-label="TODO">
    <div>Because DevTools only logs network activity when it's open.</div>
    <div>Correct.</div>
  </div>
  <div class="gc-analytics-event"
       data-category="TODO" data-value="0"
       data-label="TODO">
    <div>Because something is broken.</div>
    <div>Incorrect. Please try again.</div>
  </div>
</div>

## Feedback {: #feedback }

{% include "web/_shared/helpful.html" %}

## Draft

