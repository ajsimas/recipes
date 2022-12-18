---
layout: page
title: Recipes
---
{% assign sorted_recipes = site.posts | sort: 'title' %}
<ul>
{% for recipe in sorted_recipes %}
{% if recipe.tags contains 'recipe' %}
{% unless recipe.tags contains 'draft' %}
<li>
  <a href="{{ recipe.url }}">{{ recipe.title }}</a>
</li>
{% endunless %}
{% endif %}
{% endfor %}
</ul>

### Drafts
<ul>
{% for recipe in sorted_recipes %}
{% if recipe.tags contains 'recipe' %}
{% if recipe.tags contains 'draft' %}
<li>
  <a href="{{ recipe.url }}">{{ recipe.title }}</a>
</li>
{% endif %}
{% endif %}
{% endfor %}
</ul>