---
layout: default
title: Welcome to Anny's Comics!
---

<div class="posts">
  {% for post in site.posts %}
    {% if post.noTitle == true %}
	    <article class="post">

		      {% if site.tags != "" %}  
		        {% include collectTags.html %}
		      {% endif %}  
		          
		      <div class="center">
		        {{ post.date | date: "%B %e, %Y" }}
		        <p><span>[
		          {% for tag in post.tags %}
		            {% capture tag_name %}{{ tag }}{% endcapture %}
		            <a href="/tag/{{ tag_name }}"><code class="highligher-rouge"><nobr>{{ tag_name }}</nobr></code>&nbsp;</a>
		          {% endfor %}
		        ]</span></p>  
		        <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">
		          {{ post.excerpt }}
		        </a>          
		      </div>

	    </article>
     {% endif %}
  {% endfor %}
</div>
