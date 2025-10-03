# Semantic Tags
- Semantic means 'significance' or 'meaning'.
- These tags not just add _appearance_ to content inside element but also add _meaning_ to them.
- These describe purpose/meaning of content to not only users but also to search engine bots/crawlers/spiders or screen readers.
    - Search engine bots scan web pages to better serve info on internet according to relevance.
    - Screen readers are assistive software that convert on-screen text and images into non-visual output like synthesized speech or braille
- Provides accessiblity, more structure, better SEO, maintainability.
```html
<br> <!-- makes text bold (purely visual, non-semantic). -->
<strong> <!-- indicates text is important (semantic, and also often bold by default). -->

<i>
<em>
```
```html
<div class="top">My Blog</div>
<div class="menu"><span>Home</span> | <span>About</span></div>
<div class="content">Article goes here...</div>
<div class="bottom">© 2025</div>

<!-- vs. -->

<header>My Blog</header>
<nav>Home | About</nav>
<main>
  <article>
    <h1>Article Title</h1>
    <p>Article goes here...</p>
  </article>
</main>
<footer>© 2025</footer>
```
- Use divs/span when only CSS styling is important plus content holds no real meaning.
    - ex: A generic grid wrapper just to apply flexbox (div), A small inline piece of text you want to color differently (span).
- Use semantic tags when you want to add meaning to content with clear role not just styling.
    - ex: A copyright strip at the bottom (footer), A set of links to main pages (nav).

## Most common ones
- <header> -> Top section (logo, intro, sometimes nav).
- <nav> -> Navigation menu.
- <main> -> The unique central content of the page.
- <article> -> A self-contained piece of content that could stand alone and make sense outside the page. Blog post, forum post, product card, news story.
- <section> -> A thematic grouping of related content, usually with a heading, that contributes to the page’s structure. Logical grouping (like "Features," "Testimonials", "Contact").
- <aside> -> Sidebar, related info, ads.
- <footer> -> Bottom section (legal, contacts, links).
- <figure> + <figcaption> -> Images, charts, code snippets with captions.
- <mark> -> (highlight text),
- <time> -> (dates/times in a structured format),
- <address> -> (contact info).

# Code snippets
- pre tag: preformatted text, preserves whitespace and line breaks. 
```html
<pre>
             A
            LUT
             M
            O N
</pre>
```
- code tag: semantic tag, often wrapped with pre tag to preserve code intendation.
```html
<code>
    function greet(name) {
      console.log("Hello, " + name + "!");
    }
    greet("World");
</code>
```
