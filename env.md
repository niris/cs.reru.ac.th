---
---

{% for page in site.pages %}
{{page.name}} {{page.title}}
{% endfor %}
---
{% for document in site.documents %}
{{document.name}}
{% endfor %}
---
<ul>
{% for x in site %}
<li>{{x}}:{% if x != 'html_pages' and x != 'documents' and x != 'pages' %}{{site[x]}} <ul>{% for y in site[x] %}<li>{{y}}</li>{% endfor %}</ul>{%endif%}</li>
{% endfor %}
</ul>
