
<div class="dex_guide"><h1 class="dex_title">Futures</h1><section class="dex_document"><h1 class="dex_h0">dex_h0</h1><div class="dex_introduction">Futures is a framework for expressing asynchronous code in C++ using the Promise/Future pattern.</div><section class="dex_document_body"><h2 id="important-links-and-reso">Important links and resources <a href="#important-links-and-reso" class="headerLink">#</a></h2>

<ul>
<li>places</li>
</ul>

<h2 id="overview">Overview <a href="#overview" class="headerLink">#</a></h2>

<p>Folly&#039;s Futures is an async C++ framework inspired by Twitter&#039;s Scala Futures implementation (see <a href="https://github.com/twitter/util/blob/master/util-core/src/main/scala/com/twitter/util/Future.scala" target="_blank">Future.scala</a> and friends), and loosely builds upon the existing but anemic Futures code found in the C++11 standard (std::future) and boost::future (especially &gt;= 1.53.0).</p>

<p>Let&#039;s dive right in with a contrived and synchronous example of Futures.</p>

<div class="remarkup-code-block" data-code-lang="php"><pre class="remarkup-code"><span class="no">Promise</span><span class="o">&lt;</span><span class="no">int</span><span class="o">&gt;</span> <span class="no">p</span><span class="o">;</span>
<span class="no">Future</span><span class="o">&lt;</span><span class="no">int</span><span class="o">&gt;</span> <span class="no">f</span> <span class="o">=</span> <span class="no">p</span><span class="o">.</span><span class="nf" data-symbol-name="getFuture">getFuture</span><span class="o">();</span>
<span class="c">// ...</span>
<span class="no">p</span><span class="o">.</span><span class="nf" data-symbol-name="setValue">setValue</span><span class="o">(</span><span class="mi">42</span><span class="o">);</span> <span class="c">// or setException(...)</span>
</pre>
</div>
