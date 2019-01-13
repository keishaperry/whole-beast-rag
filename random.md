---
layout: page
title: Random
permalink: /random/
---
<script>
    var posts = []; 
    {% for post in site.posts %}
    posts.push("{{ post.url }}"); 
    {% endfor %}
    $(document).ready(function () {
        window.location = posts[Math.floor(Math.random() * posts.length)];
    });
</script>

