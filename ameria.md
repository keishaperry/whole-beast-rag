---
layout: page
title: Ameri/a
permalink: /ameria/
issue: "ameria"
---
<h2 class="uk-text-center">{{page.title}}</h2>
<div class="uk-container-small uk-grid" uk-grid>
    {% assign the_issue = site.posts | where: 'issue', "ameria" | reverse %} 
    <div class="uk-width-1-2 uk-flex-left">
    {% for post in the_issue limit:21 %} 
    <h4><a href="{{post.url}}">{{post.title}}</a></h4>
    {% endfor %}
    </div>
    <div class="uk-width-1-2 uk-flex-left">
    {% for post in the_issue offset:21 %} 
    <h4><a href="{{post.url}}">{{post.title}}</a></h4>
    {% endfor %}
    </div>
</div>