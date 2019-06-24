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

<link rel="stylesheet" href="resources/css/security-effect.css" />

## <a id="cysp">Unknown</a> <a id="chickenz" class="chicken-anim">🐔</a>

<div id="🐣">
  <button class="chicken-anim" id="chkens0">🐔</button>
  <br><button class="chicken-anim" id="chkens1">🐔</button>
  <br><button class="chicken-anim" id="chkens2">🐔</button>
  <br><button class="chicken-anim" id="chkens3">🐔</button>
  <br><button class="chicken-anim" id="chkens4">🐔</button>
  <br><button class="chicken-anim" id="chkens5">🐔</button>
  <br><button class="chicken-anim" id="chkens6">🐔</button>
  <br><button class="chicken-anim" id="chkens7">🐔</button>
  <br><button class="chicken-anim" id="chkens8">🐔</button>
  <br><br>
  <button id="cc" class="neko-btn merge shadow neko-color-green"><text class="chicken-anim" style="display:inline-block">🤔</text> 点击一下会发生什么呢？</button>
  <h6>sprite</h6>
  <h6>???</h6>
  <input id="sound-vol" type="range" min="0" max="100" />
  <input id="rate-ctr" type="range" min="50" max="400" />
  <input id="skip-ctr" type="range" min="-10" max="10" />
  <button id="skip-do" class="neko-btn merge shadow neko-color-lime">→</button>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/howler/2.1.2/howler.core.min.js" integrity="sha256-q2vnVvwrx3RbYXPyAwx7c2npmULQg2VdCXBoJ5+iigs=" crossorigin="anonymous"></script>
<script>
const byId = document.getElementById.bind(document);

onload(()=> {
  const loc = 'resources/audio/15e14b2ca405cc4a0419f4091f125b7235b8264d.mp3';
  const chilk = '🐣';

  // if WebAudio is supported
  try {
    let audio = new Audio();
    audio.src = loc;
    audio.controls = true;
    audio.autoplay = false;
    audio.hidden = true;
    document.body.appendChild(audio);
  } catch (Error) {}

  try {
    let ctx = Howler.ctx;
    let ana = ctx.createAnalyzer();
    let src = ctx.createMediaElementSource(audio);

    window.analyzer = ()=> ana;
    src.connect(ana); ana.connect(ctx.destination);
  } catch (Error) {}


  let
    rate_ctr = byId('rate-ctr'),
    skip_ctr = byId('skip-ctr')
    skip_btn = byId('skip-do');

  let pos = 0,
      skp = 0;

  skip_ctr.oninput = (line) => {
    skp = Number.parseInt(skip_ctr.value);
    console.log("New skip offset ", skp);
  };

  skip_btn.onclick = () => {
    console.log("Skipping, ", skp, pos);

    if (Howler.usingWebAudio) {
      pos=Howler.ctx.currentTime;
      Howler.ctx.currentTime = pos + skp;
    }
    else {ud83dudc14.seek(skp);}
  };

  rate_ctr.oninput = (line) => {
    let metr = Number.parseInt(rate_ctr.value) *0.01;
    ud83dudc14.rate(metr);
    console.log("New playback rate ", metr);
  };

  let lyric_points = range(1,8+1).map(i => byId(`chkens${i}`));
  for (let elem of lyric_points) {
    elem.onclick = () => {elem.innerText='🐣';elem.classList.add(chicken_anim)};
  }

  let volumer = byId('sound-vol');
  volumer.oninput = (line) => {
    let metr = Number.parseInt(volumer.value) *0.01;
    ud83dudc14.volume(metr)
    console.log("New volume ", metr);
  };

  let tried = 0; // 要按 N 次才有效果...
  let lyrics = false;

  function 壮士() {alert("🐔 LOVE YOU！");}

  let ud83dudc14 = new Howl({src:[loc],autoplay:false,onend:壮士});
  let chi = byId(chilk);
  let cc = byId('cc');

  function truncMovePoint(dx) { while (Math.trunc(dx) !==dx) {dx = dx*10;} return dx; }
  function accMovePoint(dx, greater=1) { while (dx <greater) {dx = dx*10;} return dx; }

  function pick(xs) {
    let i = truncMovePoint(Math.random());
    return xs[i %xs.length];
  }

  // Why dont use ES6 template string?
  let 鸡lyrics = "只因你太美 baby 只因你太美 baby|只因你实在是太美 baby 只因你太美 baby|迎面走来的你让我如此蠢蠢欲动|这种感觉我从未有|Cause I got a crush on you who you|你是我的我是你的谁|再多一眼看一眼就会爆炸|再近一点靠近点快被融化|想要把你占为己有baby bae|不管走到哪里都会想起的人是你 you you|我应该拿你怎样|uh 所有人都在看着你|我的心总是不安|oh 我现在已病入膏肓|eh eh 难道真的因为你而疯狂吗|我本来不是这种人|因你变成奇怪的人|第一次呀变成这样的我|不管我怎么去否认|只因你太美 baby 只因你太美 baby|只因你实在是太美 baby 只因你太美 baby|oh eh oh 现在确认地告诉我|oh eh oh 你到底属于谁|oh eh oh 现在确认地告诉我|oh eh oh 你到底属于谁 就是现在告诉我|跟着这节奏 缓缓 make wave|甜蜜的奶油 it's your birthday cake|男人们的 game call me 你恋人|别被欺骗愉快的 I wanna play|我的脑海每分每秒只为你一人沉醉|最迷人让我神魂颠倒是你身上香水|oh right baby I'm fall in love with you|我的一切你都拿走只要有你就已足够|我到底应该怎样|uh 我心里一直很不安|其他男人们的视线|Oh 全都只看向你的脸|Eh eh 难道真的因为你而疯狂吗|我本来不是这种人|因你变成奇怪的人|第一次呀变成这样的我|不管我怎么去否认|只因你太美 baby 只因你太美 baby|只因你实在是太美 baby 只因你太美 baby|我愿意把我的全部都给你|我每天在梦里都梦见你还有我闭着眼睛也能看到你|现在开始我只准你看我|I don't wanna wake up in dream 我只想看你这是真心话|只因你太美 baby 只因你太美 baby|只因你实在是太美 baby 只因你太美 baby|oh eh oh 现在确认的告诉我|oh eh oh 你到底属于谁|oh eh oh 现在确认的告诉我|oh eh oh 你到底属于谁就是现在告诉我".split("|");

  const chicken_anim = 'chicken-anim';

  // recursive callback until 鸡lyrics is empty
  let $delay_max = 1000;
  const selectJTime = ()=> accMovePoint(Math.random(), $delay_max);
  let reent;
  const 鸡你太美 = ()=>setTimeout(reent=()=> {
    if (!lyrics) return;
    let chik = 鸡lyrics.pop();
    let elem = pick(lyric_points);
    console.log("Selected: ", elem, chik);
    elem.innerText += chik + "\t";

    if (chik.length %2==0) {
      elem.classList.remove(chicken_anim);
    }

    if (鸡lyrics.length ===0) return;
    let next_time = selectJTime();
    console.log("Next launch: ", next_time);
    setTimeout(reent, next_time);

    $delay_max -= accMovePoint(Math.random(), 20);
    if ($delay_max <500) $delay_max=500;
  }, selectJTime());

  cc.onclick = ()=> {
    switch (tried) {
    case 0:
      byId('cysp').innerText = 'Chicken! You are SO PREETY!';
      ud83dudc14.once('load', ()=>ud83dudc14.play());
      cc.innerText = '好奇心害死猫！🐔';
      break;
    case 1:
      ud83dudc14.play();
      cc.innerText = '😭 不！放我出去！';
      break;
    case 2:
      lyrics = true;
      鸡你太美();
      break;
    case 3:
      break;
    case 4:
      ud83dudc14.fade(1.0, 0.0, 5000);
      break;
    default:
      alert("WARNING: κȜùηȇΓ%ƀő̌	ʦʚưɛÊȗɯȬĝŏ3ǡ˸Ŏʻ˄ČΏğķƊʣ¶ ɮ!η\"À#Γ$ɑ%ū&Į'ȥ(ȕ)α*̽+Φ,ƀ-ƿ.ʝ/Ȕ0ͫ1͖2ˍ3ȫ4ļ5ť6ƨ7$8½9Ͱ:;Ȣ<5=ˏ>Ə?̀@ͩA̧BʹCĂDʯEwF GȡHI;J KLÃMNɞOɡPđQ˩R5SɸTɕUϡVʪWΆẌYƫZ˭[Ĵ\ƚ]ˍ^ƫ_Ǒ`DaăbϑcŻdÇeĺfΉgγhĲişjBkʩlξmˢnÔoǃpɝqŸrƁsÃtǒuʮvşwƄx¬yƍzĖ{ȧ|Ŀ}ϖ~ǣ΢ΰȹŇΉ͆śŗΎ¨ş£ŅΏ½Ō˶͖͞ΆƞÙ̆ιɉ΍ɯɾşĻ@Ȇ˶ Ʈ¡¢ŷ£Ω¤Ȅ¥̏¦ĳ§Ē¨A©³ª«K¬·­ǁ®Ɔ¯´°ͅ±6²¤³ˮ´kµ͚¶·˭¸̎¹ōº¸»΋¼T½ĺ¾΃¿̄À̷ÁųÂǆÃÄ,Å˂ÆȺÇ˱ÈÉξÊËŬÌġÍɶÎǣÏ͸ÐΛÑΣÒτÓǽÔɃÕǵÖā×̇ØáÙʭÚɊÛČÜÝɋÞ˷ß˒àOá͹âɚãθäæåȕæɬçlè¢éɀêɡëȮìĭíǊî̿ïɁðàñˊò΄ó^ôͮõǫö¶÷ȂøǐùȕúόûƊüǖýîþȓÿĤĀƨāĖĂ©ăĐĄązĆćƄĈƢĉȗĊ̭ċ̼ČϓčȢĎͺďƥĐ˙đuĒēĔóĕͲĖðėϟĘðęǻĚĞěɷĜǊĝǡĞŦğɗĠ¤ġÌĢʹģOĤȻĥĦɛħ®Ĩƶĩ¡Īʟī");
      cc.innerHTML = '<img src="https://raw.githubusercontent.com/XUranus/jinitaimei/master/demo.gif" />';
      ud83dudc14.stop();
    }
    ++tried;
  };
});
</script>

$$\textbf{Quod erat demonstrandum.}$$
