---
layout: page
title: Blog
permalink: /blog/
---

<div class="home">
  <div class="post" itemscope itemtype="http://schema.org/BlogPosting" >
   
{% for post in site.categories.blog limit:5 %}

    <header class="post-header">
      <h1 itemprop="name" class="post-title">
        <a itemprop="url" class="post-link" href="{{ post.url | prepend: site.baseurl | prepend: post.baseurl }}">{{ post.title }}</a>
      </h1>
      <time itemprop="datePublished" datetime="{{ post.date | date: '%Y-%m-%d' }}">
      {{ site.locales[site.default_locale].PostDate }}{{ post.date | date: "%b %-d, %Y" }}
      </time>
      </p>
    </header>

    <article class="post-content" itemprop="articleBody">
      {{ post.longexcerpt }}
    </article> <hr />
    
{% endfor %}

  </div>
</div>
