---
keywords: fastai
title: Using JS Kernal
toc: true
badges: true
author: Yuri
categories: [jupyternotebook]
nb_path: _notebooks/2022-09-26-javascriptKernaltest.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-09-26-javascriptKernaltest.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="s2">&quot;Simple Sorting Algorythym&quot;</span><span class="p">);</span>

<span class="c1">//array of nums that are going to be sorted through</span>
<span class="kd">var</span> <span class="nx">numArr</span> <span class="o">=</span> <span class="p">[</span><span class="mf">9</span><span class="p">,</span><span class="mf">3</span><span class="p">,</span><span class="mf">1</span><span class="p">,</span><span class="mf">23</span><span class="p">,</span><span class="mf">91</span><span class="p">,</span><span class="mf">13</span><span class="p">,</span><span class="mf">1092</span><span class="p">,</span><span class="mf">72</span><span class="p">]</span>

<span class="c1">// takes an array of numbers</span>
<span class="kd">function</span> <span class="nx">sortNum</span><span class="p">(</span><span class="nx">arr</span><span class="p">){</span>

	<span class="c1">//Outer pass</span>
	<span class="k">for</span><span class="p">(</span><span class="kd">let</span> <span class="nx">i</span> <span class="o">=</span> <span class="mf">0</span><span class="p">;</span> <span class="nx">i</span> <span class="o">&lt;</span> <span class="nx">arr</span><span class="p">.</span><span class="nx">length</span><span class="p">;</span> <span class="nx">i</span><span class="o">++</span><span class="p">){</span>	
	    <span class="c1">//Inner pass</span>
	    <span class="k">for</span><span class="p">(</span><span class="kd">let</span> <span class="nx">j</span> <span class="o">=</span> <span class="mf">0</span><span class="p">;</span> <span class="nx">j</span> <span class="o">&lt;</span> <span class="nx">arr</span><span class="p">.</span><span class="nx">length</span> <span class="o">-</span> <span class="nx">i</span> <span class="o">-</span> <span class="mf">1</span><span class="p">;</span> <span class="nx">j</span><span class="o">++</span><span class="p">){</span>
    
		<span class="c1">//Value comparison using ascending order</span>
    
		<span class="k">if</span><span class="p">(</span><span class="nx">arr</span><span class="p">[</span><span class="nx">j</span> <span class="o">+</span> <span class="mf">1</span><span class="p">]</span> <span class="o">&lt;</span> <span class="nx">arr</span><span class="p">[</span><span class="nx">j</span><span class="p">]){</span>
    
		    <span class="c1">//Swapping</span>
		    <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">arr</span><span class="p">);</span>
		    <span class="p">[</span><span class="nx">arr</span><span class="p">[</span><span class="nx">j</span> <span class="o">+</span> <span class="mf">1</span><span class="p">],</span><span class="nx">arr</span><span class="p">[</span><span class="nx">j</span><span class="p">]]</span> <span class="o">=</span> <span class="p">[</span><span class="nx">arr</span><span class="p">[</span><span class="nx">j</span><span class="p">],</span><span class="nx">arr</span><span class="p">[</span><span class="nx">j</span> <span class="o">+</span> <span class="mf">1</span><span class="p">]]</span>
		<span class="p">}</span>
	    <span class="p">}</span>
	<span class="p">};</span>
	<span class="k">return</span> <span class="nx">arr</span><span class="p">;</span>
    <span class="p">};</span>
    
    <span class="nx">console</span><span class="p">.</span><span class="nx">log</span><span class="p">(</span><span class="nx">sortNum</span><span class="p">(</span><span class="nx">numArr</span><span class="p">));</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">

<div class="output_subarea output_stream output_stdout output_text">
<pre>Simple Sorting Algorythym
[ 9, 3, 1, 23, 91, 13, 1092, 72 ]
[ 3, 9, 1, 23, 91, 13, 1092, 72 ]
[ 3, 1, 9, 23, 91, 13, 1092, 72 ]
[ 3, 1, 9, 23, 13, 91, 1092, 72 ]
[ 3, 1, 9, 23, 13, 91, 72, 1092 ]
[ 1, 3, 9, 23, 13, 91, 72, 1092 ]
[ 1, 3, 9, 13, 23, 91, 72, 1092 ]
[ 1, 3, 9, 13, 23, 72, 91, 1092 ]
</pre>
</div>
</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 
