<template>
  <section class="flex-container">
    <section id="section1">
      <img
        srcset="
          https://www.ionos.com/digitalguide/fileadmin/_processed_/2/d/csm_sitemap-t_f89576c988.jpg
        "
        class="right"
      />
      <p>
        The Document Object Model, DOM for short, is a standardized programming
        interface for the structuring of HTML and XML documents. It was
        developed and released by the World Wide Consortium (W3C), the
        organization founded by web inventor Tim Berners-Lee in 1994, to design
        and establish standards for the World Wide Web.
      </p>
      <br />
      <p>
        The purpose of the Document Object Model is to make it as easy as
        possible for programmers to access a web project’s components so that
        they can add to, delete and edit the project’s content, attributes, and
        styles. DOM serves as a platform-independent and language-neutral link
        between script languages such as JavaScript and the basic web document,
        as it depicts the structure of the document in a tree structure in which
        every node is an independent, selectable object. Because of this
        structure, one also refers to this type of displayed web project version
        as a DOM tree.
      </p>
    </section>

    <section id="section2">
      <h3>API</h3>
      <ol>
        <li>const linkRef = document.querySelector(NODE);</li>
        <li>let child = Document.createElement(NODE);</li>
        <li>linkRef.appendChild(child)</li>
      </ol>
    </section>
  </section>

  <h3>Example</h3>
  <div id="example">
    <label for="item">Enter new subject:</label>
    <input type="text" name="item" id="item" />
    <button>Add subject</button>
  </div>

  <ul></ul>
</template>

<script scoped>
export default {
  name: 'Main',
};
</script>

<style>
body {
  font-family: Verdana;
}

h1 {
  text-align: center;
}

h2 {
  text-align: center;
  border-bottom-style: solid;
}

img {
  height: 100px;
  width: 200px;
  float: left;
}

.flex-container {
  display: flex;
}

#item {
  text-align: right;
}
</style>
