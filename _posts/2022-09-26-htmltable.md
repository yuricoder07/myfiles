---
keywords: fastai
title: Using JS to create HTML
toc: true
badges: true
author: Yuri
categories: [jupyternotebook]
nb_path: _notebooks/2022-09-26-htmltable.ipynb
layout: notebook
---

<!--
#################################################
### THIS FILE WAS AUTOGENERATED! DO NOT EDIT! ###
#################################################
# file to edit: _notebooks/2022-09-26-htmltable.ipynb
-->

<div class="container" id="notebook-container">
        
    {% raw %}
    
<div class="cell border-box-sizing code_cell rendered">
<div class="input">

<div class="inner_cell">
    <div class="input_area">
<div class=" highlight hl-javascript"><pre><span></span><span class="c1">//Define data</span>
<span class="kd">function</span> <span class="nx">Person</span><span class="p">(</span><span class="nx">name</span><span class="p">,</span> <span class="nx">role</span><span class="p">)</span> <span class="p">{</span>
	<span class="k">this</span><span class="p">.</span><span class="nx">name</span> <span class="o">=</span> <span class="nx">name</span><span class="p">;</span>
	<span class="k">this</span><span class="p">.</span><span class="nx">role</span> <span class="o">=</span> <span class="nx">role</span><span class="p">;</span>
    <span class="p">}</span>

<span class="nx">Person</span><span class="p">.</span><span class="nx">prototype</span><span class="p">.</span><span class="nx">setRole</span> <span class="o">=</span> <span class="kd">function</span><span class="p">(</span><span class="nx">role</span><span class="p">)</span> <span class="p">{</span>
	<span class="k">this</span><span class="p">.</span><span class="nx">role</span> <span class="o">=</span> <span class="nx">role</span><span class="p">;</span>
    <span class="p">}</span>
<span class="nx">Person</span><span class="p">.</span><span class="nx">prototype</span><span class="p">.</span><span class="nx">toJSON</span> <span class="o">=</span> <span class="kd">function</span><span class="p">()</span> <span class="p">{</span>
	<span class="kr">const</span> <span class="nx">obj</span> <span class="o">=</span> <span class="p">{</span><span class="nx">name</span><span class="o">:</span> <span class="k">this</span><span class="p">.</span><span class="nx">name</span><span class="p">,</span> <span class="nx">role</span><span class="o">:</span><span class="k">this</span><span class="p">.</span><span class="nx">role</span><span class="p">};</span>
	<span class="kr">const</span> <span class="nx">json</span> <span class="o">=</span> <span class="nx">JSON</span><span class="p">.</span><span class="nx">stringify</span><span class="p">(</span><span class="nx">obj</span><span class="p">);</span>
	<span class="k">return</span> <span class="nx">json</span><span class="p">;</span>
    <span class="p">}</span>
    
<span class="c1">// Creating data and putting it into a list</span>
<span class="kd">var</span> <span class="nx">Yuri</span> <span class="o">=</span> <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Yuri&quot;</span><span class="p">,</span> <span class="s2">&quot;DevOps&quot;</span><span class="p">);</span>
<span class="kd">var</span> <span class="nx">Tanay</span> <span class="o">=</span> <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Tanay&quot;</span><span class="p">,</span> <span class="s2">&quot;Scrum Master&quot;</span><span class="p">);</span>
<span class="kd">var</span> <span class="nx">Harsha</span> <span class="o">=</span> <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Harsha&quot;</span><span class="p">,</span> <span class="s2">&quot;Frontend&quot;</span><span class="p">);</span>
<span class="kd">var</span> <span class="nx">Sachit</span> <span class="o">=</span> <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Sachit&quot;</span><span class="p">,</span> <span class="s2">&quot;Backend&quot;</span><span class="p">);</span>
<span class="kd">var</span> <span class="nx">Raunak</span> <span class="o">=</span> <span class="k">new</span> <span class="nx">Person</span><span class="p">(</span><span class="s2">&quot;Raunak&quot;</span><span class="p">,</span> <span class="s2">&quot;Backend&quot;</span><span class="p">);</span>

<span class="nx">storedInfo</span> <span class="o">=</span> <span class="p">[</span><span class="nx">Yuri</span><span class="p">,</span> <span class="nx">Tanay</span><span class="p">,</span> <span class="nx">Harsha</span><span class="p">,</span> <span class="nx">Sachit</span><span class="p">,</span> <span class="nx">Raunak</span><span class="p">];</span>

<span class="c1">//Make a object to hold the data</span>
<span class="kd">function</span> <span class="nx">infoStorage</span><span class="p">(</span><span class="nx">storedInfo</span><span class="p">)</span> <span class="p">{</span>
	<span class="k">this</span><span class="p">.</span><span class="nx">storedInfo</span> <span class="o">=</span> <span class="nx">storedInfo</span><span class="p">;</span>
    <span class="p">}</span>
    
    <span class="c1">// Type Object that holds the data</span>
    <span class="nx">infoHolder</span> <span class="o">=</span> <span class="k">new</span> <span class="nx">infoStorage</span><span class="p">(</span><span class="nx">storedInfo</span><span class="p">);</span>
    <span class="c1">//HTML conversion method</span>
    <span class="nx">infoStorage</span><span class="p">.</span><span class="nx">prototype</span><span class="p">.</span><span class="nx">_toHtml</span> <span class="o">=</span> <span class="kd">function</span><span class="p">()</span> <span class="p">{</span>
	<span class="kd">var</span> <span class="nx">style</span> <span class="o">=</span> <span class="p">(</span>
	  <span class="s2">&quot;display:inline-block;&quot;</span> <span class="o">+</span>
	  <span class="s2">&quot;border: 2px solid grey;&quot;</span> <span class="o">+</span>
	  <span class="s2">&quot;box-shadow: 0.8em 0.4em 0.4em grey;&quot;</span>
	<span class="p">);</span>
      
	<span class="kd">var</span> <span class="nx">table</span> <span class="o">=</span> <span class="s2">&quot;&quot;</span><span class="p">;</span>
	<span class="nx">table</span> <span class="o">+=</span> <span class="s2">&quot;&lt;tr&gt;&quot;</span><span class="p">;</span>
	<span class="nx">table</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Name&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
	<span class="nx">table</span> <span class="o">+=</span> <span class="s2">&quot;&lt;th&gt;&lt;mark&gt;&quot;</span> <span class="o">+</span> <span class="s2">&quot;Role&quot;</span> <span class="o">+</span> <span class="s2">&quot;&lt;/mark&gt;&lt;/th&gt;&quot;</span><span class="p">;</span>
	<span class="nx">table</span> <span class="o">+=</span> <span class="s2">&quot;&lt;/tr&gt;&quot;</span><span class="p">;</span>
    
	<span class="c1">//Go through all data and each data&#39;s properties in a table format</span>
	<span class="k">for</span> <span class="p">(</span><span class="kd">var</span> <span class="nx">row</span> <span class="k">of</span> <span class="k">this</span><span class="p">.</span><span class="nx">storedInfo</span><span class="p">)</span> <span class="p">{</span>
	    <span class="nx">table</span> <span class="o">+=</span> <span class="s2">&quot;&lt;tr&gt;&quot;</span><span class="p">;</span>
	    <span class="nx">table</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">name</span><span class="p">;</span>
	    <span class="nx">table</span> <span class="o">+=</span> <span class="s2">&quot;&lt;td&gt;&quot;</span> <span class="o">+</span> <span class="nx">row</span><span class="p">.</span><span class="nx">role</span> <span class="o">+</span> <span class="s2">&quot;&lt;/td&gt;&quot;</span><span class="p">;</span>
	    <span class="nx">table</span> <span class="o">+=</span> <span class="s2">&quot;&lt;tr&gt;&quot;</span>
	<span class="p">}</span>
	 <span class="c1">//Return table</span>
	<span class="k">return</span> <span class="p">(</span>
	  <span class="s2">&quot;&lt;div style=&#39;&quot;</span> <span class="o">+</span> <span class="nx">style</span> <span class="o">+</span> <span class="s2">&quot;&#39;&gt;&quot;</span> <span class="o">+</span>
	    <span class="s2">&quot;&lt;table&gt;&quot;</span> <span class="o">+</span>
		<span class="nx">table</span> <span class="o">+</span>
	    <span class="s2">&quot;&lt;/table&gt;&quot;</span> <span class="o">+</span>
	  <span class="s2">&quot;&lt;/div&gt;&quot;</span>
	<span class="p">);</span>
      <span class="p">};</span>
      
      <span class="c1">// IJavaScript HTML processor receive parameter of defined HTML fragment</span>
      <span class="nx">$$</span><span class="p">.</span><span class="nx">html</span><span class="p">(</span><span class="nx">infoHolder</span><span class="p">.</span><span class="nx">_toHtml</span><span class="p">());</span>
</pre></div>

    </div>
</div>
</div>

<div class="output_wrapper">
<div class="output">

<div class="output_area">


<div class="output_html rendered_html output_subarea output_execute_result">
<div style='display:inline-block;border: 2px solid grey;box-shadow: 0.8em 0.4em 0.4em grey;'><table><tr><th><mark>Name</mark></th><th><mark>Role</mark></th></tr><tr><td>Yuri<td>DevOps</td><tr><tr><td>Tanay<td>Scrum Master</td><tr><tr><td>Harsha<td>Frontend</td><tr><tr><td>Sachit<td>Backend</td><tr><tr><td>Raunak<td>Backend</td><tr></table></div>
</div>

</div>

</div>
</div>

</div>
    {% endraw %}

</div>
 
