---
layout: page
title: Events
permalink: /events/
---

<div class="home">
  <div class="post" itemscope itemtype="http://schema.org/BlogPosting" >
   
{% for event in site.categories.events limit:5 %}

    <header class="post-header">
      <h1 itemprop="name" class="post-title">
        <a itemprop="url" class="post-link" href="{{ event.url | prepend: site.baseurl | prepend: event.baseurl }}">{{ event.title }}</a>
      </h1>
      <time itemprop="datePublished" datetime="{{ event.date | date: '%Y-%m-%d' }}">
      {{ site.locales[site.default_locale].PostDate }}{{ event.date | date: "%b %-d, %Y" }}
      </time>
      </p>
    </header>

    <article class="post-content" itemprop="articleBody">
      {{ event.longexcerpt }}
    </article> <hr />
    
{% endfor %}

  </div>
</div>



