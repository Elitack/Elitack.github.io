---
layout: category
title: Category
---

<section class="content">
	<div class="content-cnt fn-clear">
		<div class="main">
		{% for cat in site.categories %}
		<article class="main-excerpt fn-clear">
            <h3 class="category-title"><li class="listing-seperator" id="{{ cat[0] }}">{{ cat[0] }}</li></h3>  
            {% for post in cat[1] %}
            <h6 class="category-artical">
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&#9675;&nbsp;
            <time datetime="{{ post.date | date:"%Y-%m-%d" }}">{{ post.date | date:"%Y-%m-%d" }}</time>
            <a href="{{ site.url }}{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a>
            </h6>
			{% endfor %}
		</article>
		{% endfor %}
		</div>
	</div>
</section>

