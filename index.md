layout: default title: Home

<div class="hero-section">
<h1>{{ site.title }}</h1>
<p class="subtitle">{{ site.description }}</p>

<div class="substack-form">
<form action="{{ site.newsletter_action_url }}" method="post">
<input type="email" name="email" placeholder="Type your email..." required>
<button type="submit">Subscribe</button>
</form>
<p class="small">Join 500+ readers. No spam, ever.</p>
</div>
</div>

<hr>

Recent Posts

<ul class="post-list">
{% for post in site.posts limit:5 %}
<li>
<span class="post-date">{{ post.date | date: "%b %d, %Y" }}</span>
<h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
<p>{{ post.excerpt | strip_html | truncatewords: 25 }}</p>
</li>
{% endfor %}
</ul>

<a href="/archive" class="view-all">View all posts →</a>
