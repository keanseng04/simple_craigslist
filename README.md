<div class="container">
<div id="challenge" class="row">
<div class="col-sm-8">
<div class="row">
<div class="col-sm-12">
<div class="tab-content">
<div id="body" class="tab-pane fade in active">

We're going to build a simple version of Craigslist. This will be your first web application that uses multiple models.

Keep in mind that this is not substantially different than a command-line version. Instead of reading in command-line arguments, we read in URL parameters. Instead of printing to the console, we print HTML and CSS.

We'll only have two models in a one-to-many relationship; no different than your command-line TODO app.

As with all the Sinatra apps, start with the <a href="http://ge.tt/8fpASR22/v/0?c">Code Division Sinatra Skeleton</a>
<h2>Learning Goals</h2>
<ul>
	<li>Deepen your ActiveRecord skills around associations.</li>
	<li>Learn how to implement all four parts of <a href="http://en.wikipedia.org/wiki/Create,_read,_update_and_delete">CRUD</a>: create, read, update, and delete.</li>
</ul>
<h2>Objectives</h2>
<h3>Wireframe With Your Pair</h3>
Never heard of a web wireframe? Check out <a href="http://en.wikipedia.org/wiki/Website_wireframe">what Wikipedia has to say</a>. <strong>TL;DR</strong> -- figure out what <em>pages</em> your app needs, then sketch-out the basic <em>layout</em> of each and the <em>connections</em> between them.

The application will have two core models: <code>Post</code> and <code>Category</code>. A <code>Post</code> belongs to a <code>Category</code> and a <code>Category</code>has many <code>Posts</code>.

A <code>Category</code> is something like "Apartment Rentals" or "Auto Parts."

Sit down and work out with your pair what pages you're going to be building. At a minimum, you'll need:
<ol>
	<li>A page that lists all the categories</li>
	<li>A page that lists all the postings in a given category</li>
	<li>A page that lets someone create a new posting in a given category</li>
	<li>A page that lets someone who has created a page return to edit/update the page</li>
</ol>
If you're never used Craigslist, it doesn't have any kind of user authentication. Instead, when someone creates a post they're given a special "secret" URL that grants them powers to edit that post that looks like
<div class="highlight">
<pre>http://craigslist.com/post/123/edit?key<span class="o">=</span>kjansd812
</pre>
</div>
The key is randomly generated. The person is given their "edit URL" after they successfully create a post. Anyone with this URL can edit the post.

Think about this like a real web application you might want someone to use. What fields should a <code>Post</code> have?

A price, probably. What should the column type of a money-related column be?

An email, so the poster could be contacted. Title, description, etc.

Spend time enumerating the pages, deciding what should be displayed on each one.
<h3>Controller Structure</h3>
Our controller structure will be more complicated. We'll want URLs that look like <code>/categories/123</code> and <code>/posts/456</code>. We'll be using both <code>get</code> and <code>post</code> methods.

To create a new <code>Post</code>, for example, we'd want to submit an HTML form using the POST http method to the <code>/posts</code>URL, like so:
<div class="highlight">
<pre>&lt;form <span class="nv">action</span><span class="o">=</span><span class="s2">"/posts"</span> <span class="nv">method</span><span class="o">=</span><span class="s2">"post"</span>&gt;
  &lt;!-- other form elements here --&gt;
&lt;/form&gt;
</pre>
</div>
and to update an existing record (say with id <code>1234</code>) we'd want to post to <code>/posts/1234</code>.

Controllers should either redirect to another URL or render a page. Typically, a page loaded via HTTP POST will redirect to an appropriate URL if a request succeeds and render an error page, otherwise.
<h3>Ship it!</h3>
Make sure the core features work. We should be able to download your app, run it, and do the follow:
<ol>
	<li>Choose a category to browse</li>
	<li>View all postings in a particular category</li>
	<li>View a particular posting</li>
	<li>Create my own posting</li>
	<li>Edit my postings by using the "secret key" that I get after creating my posting</li>
</ol>
<h3>Add One Final Feature</h3>
One last feature to add: the "this is awesome" feature. What does awesome mean? It can mean anything. The code is awesome, there are new awesome features, the design is awesome.

We'll be picking one pair at random tomorrow morning to show off their version of Craigslist. They'll get a full-on UX and code review.

This isn't a race; there's no finish line, only a deadline (tomorrow, duh!). Take the time to make this application something you're proud of. It doesn't have to be flashy ‰ÛÓ it could be a difficult technical hurdle you overcame.

</div>
</div>
</div>
</div>
</div>
</div>
</div>
&nbsp;
