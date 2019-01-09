---
layout: page
title: Edge
permalink: /edge/
issue: "edge"
---
<h2 class="uk-text-center">{{page.title}}</h2>
<div class="uk-container-small uk-grid" uk-grid>
{% assign the_issue = site.posts | where: 'issue', "edge" | reverse %} 
<div class="uk-width-1-2">
{% for post in the_issue limit:33 %} 
<h4><a href="{{post.url}}">{{post.title}}</a></h4>
{% endfor %}
</div>
<div class="uk-width-1-2">
{% for post in the_issue offset:33 %} 
<h4><a href="{{post.url}}">{{post.title}}</a></h4>
{% endfor %}
</div>
<div class="clearfix"></div>
</div>