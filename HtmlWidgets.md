# Advanced interactive component test

#### HTML Widgets

<noframes>Well, missing a embed from YouTube, right<br></noframes>

<iframe width="853" height="480" src="https://www.youtube.com/embed/2MsN8gpT6jY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<noscript>Well, I can't handle the (+) calculation when JavaScript is not enabled :-(<br></noscript>

<form oninput="x.value=Number.parseInt(a.value)+Number.parseInt(b.value);document.getElementById('intro-typesetting-p').value=x.value">
  0<input type="range" id="a" value="50">100
  +<input type="number" id="b" value="50" max="100">
  = <output name="x" for="a b"></output>
</form>

<progress id="intro-typesetting-p" value="0" min="0" max="150"></progress>
<br>
<meter value="2" min="0" max="10">2 out of 10</meter>
<br>

<select>
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="opel">Opel</option>
  <option value="audi">Audi</option>
</select>

<optgroup label="German Cars optgroup"></optgroup>
<select>
  <option value="volvo">Volvo</option>
  <option value="saab">Saab</option>
  <option value="mercedes">Mercedes</option>
  <option value="audi">Audi</option>
</select>
<br>
<textarea rows="4" cols="50">
Input !
</textarea>
<br>
<dialog id="intro-typesetting-dialog"><span style="color:red">WARNING!!!</span> Running JavaScript thread spawn bomb...</dialog>
<br>
<input type="button" onclick="document.getElementById('intro-typesetting-dialog').setAttribute('open', '')" value="Destory" />
<br>
<form>
  <fieldset>
    <legend>New user:</legend>
    Name: <input type="text" placeholder="you name" maxlength="10" value="duangsuse"><br>
    Age: <input type="number" max="80" value="17"><br>
    Gender: <select>
      <option value="♂">Boy</option>
      <option value="♀">Girl</option>
    </select>
  </fieldset>
</form>
<br>
<form action="//github.com/search" method="get">
  <summary>GitHub Search</summary>
  Type: <input type="text" name="type" value="Repositories"><br>
  Query: <input type="text" name="q" value="Compiler"><br>
  Sorted By: <input type="text" name="s" value="stars"><br>
  Order: <select name="o">
  <!-- 箭头从小值指向大值 -->
    <option value="asc">Ascending ↓</option>
    <option value="desc">Descending ↑</option>
  </select>
  <input type="submit" value="Submit 👓">
</form>

### Reference stylesheet and JavaScript tag

[Neko CSS](https://neko-dev.github.io/neko.css/)

```html
<link rel="stylesheet" type="text/css" href="https://neko-dev.github.io/neko.css/dist/css/neko.css">
```

<link rel="stylesheet" type="text/css" href="https://neko-dev.github.io/neko.css/dist/css/neko.css">

<script type="text/javascript">
function sety(s) {document.getElementsByTagName('output')['y'].innerHTML=s;}
</script>
<button id="intro_typesetting_neko_ia" class="neko-btn merge shadow neko-color-green" onclick="sety('<var>dr</var>oid 📱')">Android</button>
<button id="intro_typesetting_neko_ib" class="neko-btn merge shadow neko-color-blue" onclick="sety('win 🖥')">Windows</button>
<br>
<output name="y" for="intro_typesetting_neko_ia intro_typesetting_neko_-_ib"></output>

### MathJax 编写的 TeX 数学公式

<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-AMS-MML_HTMLorMML" defer></script>

Y Combinator
$$Y = \lambda f. (\lambda c. f (c c))^2$$

Equation array
$$
\begin{eqnarray}
 f_p(x) & = & \sum_{j=0}^{n} c_j \phi(||x - x_j||)  \\
& = & \sum_{j=0}^{n} c_j \phi_j(x) \\
& = & c_0 \phi_0(x) + c_1 \phi_1(x) + \cdots + c_n \phi_n(x)
\end{eqnarray}
$$

Fibonacci program in Haskell
$$
\begin{eqnarray}
fib & 1 = 1 \\
fib & 2 = 1 \\
fib & n & \\
&|& n >0 & = & (fib n - 1) + (fib n - 2) \\
&|& otherwise & = & 0
\end{eqnarray}
$$

$$\sum_{n=1}^\infty 1/n^2 = \frac{\pi^2}{6}$$

$$(varsupsetneq)\varsupsetneq (supset)\supset (sqsupseteq)\sqsupseteq (star)\star (ast)\ast$$

$$f(a) = \frac{1}{2\pi i} \oint\frac{f(z)}{z-a}dz$$

$$
\hat{h}(t) = \sum_{k = 1}^{L} a_k(t^i_a)\cos(2\pi k f_0(t^i_a)(t - t^i_a) + \phi_k(t^i_a))
$$

$$\forall{a\in{\mathbb{Q}}}. a+n=n+a$$

$$\exists{n}. n-1=0$$

$$p \Rightarrow q \Rightarrow (p\land q)$$

$$p \Leftrightarrow q = (p \rightarrow q) \land (q \rightarrow p)$$

$$((p \lor q) \Rightarrow r) \Leftrightarrow (p \Rightarrow r) \land (q \Rightarrow r)$$

$$\mathit{R} \text{ is reflexive } \Leftrightarrow \forall{x}. (x \mathit{R} x)$$

$$\mathit{R} \text{ is symmetry } \Leftrightarrow (a \mathit{R} b) \Rightarrow (b \mathit{R} a)$$

$$\mathit{R} \text{ is transitive } \Leftrightarrow (a \mathit{R} b) \Rightarrow (b \mathit{R} c) \Rightarrow (a \mathit{R} c)$$

$$\mathit{R} \text{ is commutative } \Leftrightarrow (a \mathit{R} b) \Leftrightarrow (b \mathit{R} a)$$

$$\mathit{R} \text{ is associative } \Leftrightarrow (a \mathit{R} b) \mathit{R} c \Leftrightarrow a \mathit{R} (b \mathit{R} c)$$

$$Algorithms + Data Structures = Programs$$

$$Fix(f)=Asc(f)\cap Desc(f)$$

$$\forall x’ \in \mathit{Asc}(f) \ . \ f^i(x’) \sqsubseteq f^{i+1}$$


### echarts 数据图表

#### BarChart

<script src="https://www.echartsjs.com/examples/vendors/echarts/echarts.min.js" defer></script>

<style>
#chart { width: 512px; height: 300px }
</style>
<div id="chart"></div>
<script type="text/javascript">
const onload = (fn)=> {
  let bus=document.addEventListener.bind(document, 'DOMContentLoaded');
  bus(fn); };

onload(function(){
var testChart = echarts.init(document.getElementById('chart'));

var option = {
  title: { text: '小林家的苹果派' },
  toolbox: {
      feature: {
          dataZoom: { yAxisIndex: 'none' },
          restore: {},
          saveAsImage: {}
      }
  },
  tooltip: {},
  dataZoom: [
      {
          show: true,
          realtime: true,
          start: 0,
          end: 512
      },
      {
          type: 'inside',
          realtime: true,
          start: 0,
          end: 512
      }
  ],
  legend: { data: ['苹果派份数'], x: 'middle' },
  xAxis: {
      data: ['龙 A', '龙 B', '龙 C', '小林']
  },
  yAxis: {},
  series: [{
      name: '苹果派份数',
      type: 'bar',
      data: ['2', '1', '4', '9']
  }]
};

testChart.setOption(option);
});
</script>

#### Plot

<style>
#chart2 { width: 512px; height: 300px }
</style>
<div id="chart2"></div>

<script>
function range(start, stop, step = 1) {
  let res = [];
  for (let i=start; i<stop; i+=step) {
    res.push(i);
  } return res;
}

/**
Now I know Object.assign is more efficient...
*/
function copy(obj) {return Object.assign({}, obj);}
function mix(obj, ext) {
  let names /*It's enough.*/ = Object.getOwnPropertyNames(ext);
  let renew = copy(obj);
  for (let name of names) {
    renew[name] = ext[name];
  }
  return renew;
}

onload(() => {
  let chart2 = echarts.init(document.getElementById('chart2'));

  let xrange = range(0,100,1);
  let type = 'value';
  let datazoom_defs = { realtime: true, start: 0, end: 512 };
  let line_defs = { type: 'line', smooth: true };

  let sinys = mix(line_defs, {data:xrange.map(Math.sin)});

  let {cos, tan, asin, acos, tanh, exp, log, hypot, fround, random, pow, trunc} = Math;

  let funs = [cos, tan, asin, acos, tanh, exp, log, hypot, fround, random, pow, trunc];

  let option = {
    title: { text: 'Triangle waves and more' },
    xAxis: { type, data: xrange },
    yAxis: { type },
    tooltip: { trigger: 'axis' },
    toolbox: {
        feature: {
            dataZoom: { yAxisIndex: 'none' },
            restore: {}, saveAsImage: {}}},
    dataZoom: [
        mix(datazoom_defs, {show: true}),
        mix(datazoom_defs, {type: 'inside'})],

    legend: mix({ x: 'middle' }, {data: funs.map(f => f.name)}),
    series: funs.map(f => mix(line_defs, {name:f.name, data:xrange.map(f)}))
  }

  chart2.setOption(option);
});
</script>

$$\textbf{Quod erat demonstrandum.}$$
