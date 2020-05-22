---
layout: default
title: Welcome to Anny's Comics!
---

<div class="posts">
<form style="border:1px solid #ccc;padding:3px;text-align:center;" action="https://tinyletter.com/badaboot" method="post" target="popupwindow" onsubmit="window.open('https://tinyletter.com/badaboot', 'popupwindow', 'scrollbars=yes,width=800,height=600');return true"><p><label for="tlemail">Subscribe to get the latest comics!</label></p><p><input type="text"  placeholder="Email address" style="width:140px" name="email" id="tlemail" /></p><input type="hidden" value="1" name="embed"/><input type="submit" value="Subscribe" /><p><a href="https://tinyletter.com" target="_blank">powered by TinyLetter</a></p></form>
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
